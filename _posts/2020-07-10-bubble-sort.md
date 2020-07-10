---
layout: post
title:  "버블정렬"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
N개이 숫자가 입력되면 오름차순으로 정렬하여 출력하는 프로그램을 작성하세요.
정렬하는 방법은 버블정렬입니다.



▣ 입력설명 

첫 번째 줄에 자연수 N(1<=N<=100)이 주어집니다.
두 번째 줄에 N개의 자연수가 공백을 사이에 두고 입력됩니다. 각 자연수는 정수형 범위 안에
있습니다. 

▣ 출력설명 

오름차순으로 정렬된 수열을 출력합니다.


▣ 입력 예제 1
```
6
13 5 11 7 23 15


```

▣ 출력 예제 1
```
5 7 11 13 15 23

```

### Solution
{% highlight cpp %}
#include<stdio.h>
int main(){
	freopen("input.txt", "rt", stdin);
	int n;
	scanf("%d", &n);
	
	int arr[100];
	for(int i = 0; i < n; i++){
		scanf("%d", &arr[i]);
	}
	
	for(int i = 0; i < n ; i++){
		int temp = 0;
		for(int j=0; j < n-1-i; j++){
			
			if(arr[j]> arr[j+1]){
				temp = arr[j+1];
				arr[j+1] = arr[j];
				arr[j] = temp;
			}
		}
	}
	
	for(int i = 0; i < n; i++){
		printf("%d ", arr[i]);
	}

	return 0;
}
{% endhighlight %}


