---
layout: post
title:  "Least Recently Used(카카오 캐시 문제 변형)"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question

<img src="/assets/posts/2020-07-13-algorithm-LRU.png" title="Explation image">



▣ 입력설명 

첫 번째 줄에 캐시의 크기인 S(3<=S<=10)와 작업의 개수 N(5<=N<=1,000)이 입력된다.
두 번째 줄에 N개의 작업번호가 처리순으로 주어진다. 작업번호는 1 ~100 이다.


▣ 출력설명 

마지막 작업 후 캐시메모리의 상태를 가장 최근 사용된 작업부터 차례로 출력합니다.

▣ 입력 예제 1
```
5 9
1 2 3 2 6 2 3 5 7



```

▣ 출력 예제 1
```
7 5 3 2 6

```

```
캐시 메모리 상태 변화
1 0 0 0 0
2 1 0 0 0
3 2 1 0 0
2 3 1 0 0
6 2 3 1 0
2 6 3 1 0
3 2 6 1 0
5 3 2 6 1
7 5 3 2 6

```

### Solution
{% highlight cpp %}
#include<stdio.h>
int main(){
//	freopen("input.txt", "rt", stdin);
	int arrNum;
	scanf("%d", &arrNum);
	int arr [arrNum] = {0,};
	
	int inputCnt;
	scanf("%d", &inputCnt);
	int temp = 0;
	for(int i = 0; i < inputCnt; i++){

		scanf("%d", &temp);
		bool hasSameNum = false;
		int j = 0;
		for(j = 0; j < arrNum; j++){
			
			if(arr[j] == temp){
				hasSameNum = true;
				break;
			}
		}
		
		int swap;
		if(hasSameNum){
			for(int z = j; z > 0; z--){
				arr[z] = arr[z-1];
			}
			arr[0] = temp;
			
		}else{
			for(int z = arrNum-1; z > 0; z--){
				arr[z] = arr[z-1];
			}
			arr[0] = temp;
		}
	}
	
	for(int i = 0; i < arrNum; i++){
		printf("%d ", arr[i]);
	}
	
	return 0;
}

{% endhighlight %}


