---
layout: post
title:  "배열의 회전"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
9개의 자연수를 배열에 입력하고, K가 주어 지면 배열을 K번 회전한 후 출력하는 프로그 램을 작성하세요
```
5 9 6 11 33 21 66 15 35
9 6 11 33 21 66 15 35 5 
```
위의 그림은 배열의 한 번 회전이다. 실제 배열에 값을 넣고 값을 K번 이동한 후 배열의 내용을 0번 인덱스부터 8번 인덱스까 지 출력해야 합니다. 다른 방법은 안됩니다

▣ 입력설명 

첫 번째 줄에 9개의 숫자가 입력되고, 두 번 째 줄에 K(1<=K<=20)가 주어집니다.

▣ 출력설명 

첫 번째 줄에 배열의 출력합니다.

▣ 입력 예제 1
```
9 12 67 15 23 271 77 35 87
1
```

▣ 출력 예제 1
```
12 67 15 23 271 77 35 87 9

```
▣ 입력 예제 2
```
5 9 6 11 33 21 66 15 35
3
```

▣ 출력 예제 2
```
11 33 21 66 15 35 5 9 6

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


