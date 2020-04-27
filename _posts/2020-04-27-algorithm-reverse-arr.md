---
layout: post
title:  "배열의 역순 출력"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
첫 번째 줄에 100이하의 자연수 N이 주어진 다. 두 번째 줄에 N개의 배열원소가 주어진다.
만약 C가 50 이면 위 조건을 만족하는 두 자리 숫자는 21, 31, 32, 41, 42, 43 으로 6개 이다.

▣ 입력설명 

첫 번째 줄에 배열을 역순으로 출력한다.

▣ 출력설명 

첫 번째 줄부터 모든 경우의 수를 출력한다. 마지막 줄에 총 개수도 출력한다.

▣ 입력 예제 1
```
5 
3 6 2 7 1
```

▣ 출력 예제 1
```
1 7 2 6 3

```
▣ 입력 예제 2
```
7 
6 3 7 8 4 9 5
```

▣ 출력 예제 2
```
5 9 4 8 7 3 6

```

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	int n;
	scanf("%d", &n);
	int arr[n];

	for(int i=0; i<n; i++){
		scanf("%d", &arr[i]);
	}

	for(int i=n-1; i>=0; i--){
		printf("%d ", arr[i]);
	}
	return 0;
}

{% endhighlight %}


