---
layout: post
title:  "자리 찾기"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
100 이하의 자연수 N이 주어지고, N 크기의 오름차순으로 정렬된 배열이 있다. 100 이하의 자연수 M이 주어지면 이 자연수 M을 배열의 오름차순을 유지하는 자기 자리 에 삽입하는 프로그램을 작성하세요. 만약 1 5 7 9 12의 오름차순 정렬된 배열이 주어지고, M=6이면 배열의 5와 7사이에 삽 입해 1 5 6 7 9 12 를 출력하면 된다.

▣ 입력설명 

첫 번째 줄에 100 이하의 자연수 N이 주어 진다. 두 번째 줄에 오름차순으로 정렬된 N 크기의 배열 원소가 주어진다. 세 번째 줄에 자연수 M이 주어진다.

▣ 출력설명 

첫 번째 줄에 M이 삽입된 배열을 출력한다.

▣ 입력 예제 1
```
5 
1 3 7 9 15 
8
```

▣ 출력 예제 1
```
1 3 7 8 9 15

```
▣ 입력 예제 2
```
7 
11 15 19 23 27 32 36 
21

```

▣ 출력 예제 2
```
11 15 19 21 23 27 32 36 

```

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){

	int arr[100];
	int n;
	scanf("%d", &n);
	
	for(int i=0; i<n; i++){
		scanf("%d", &arr[i]);
	}
	
	int insertVal;
	scanf("%d", &insertVal);
	for(int i = 0; i < n; i++){
		if(arr[i] > insertVal){
			for(int j = n; j > i; j--){
				arr[j] = arr[j-1];				
			}
			arr[i] = insertVal;			
			break;
		}
	}
	
	for(int i=0; i< n+1; i++){
		printf("%d ", arr[i]);
	}
	
	return 0;
}

{% endhighlight %}


