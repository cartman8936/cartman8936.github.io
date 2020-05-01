---
layout: post
title:  " 2차원 배열 출력 1"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
10 이하의 자연수 N이 입력되면 N*N 크기의 2차원 배열을 이용하여 아래와 같이 출력하 는 프로그램을 작성하세요.



▣ 입력설명 

첫 번째 줄에 10이하의 자연수 N이 주어진 다.

▣ 출력설명 

2채원 배열을 출력한다.

▣ 입력 예제 1
```
5

```

▣ 출력 예제 1
```
  5 10 15 20 25
  4  9 14 19 24  
  3  8 13 18 23  
  2  7 12 17 22  
  1  6 11 16 21

```

▣ 입력 예제 2
```
7

```

▣ 출력 예제 2
```
  7 14 21 28 35 42 49
  6 13 20 27 34 41 48
  5 12 19 26 33 40 47
  4 11 18 25 32 39 46
  3 10 17 24 31 38 45
  2  9 16 23 30 37 44
  1  8 15 22 29 36 43

```

### Solution

{% highlight cpp %}
#include<stdio.h>


int arr[10][10];

int main(){
	
	int n;
	scanf("%d", &n);
		
	for(int i= 0; i < n; i++){
		for(int j = 0; j  < n ; j++){
			arr[i][j] = (n-i) + n * j;		
		}
	}
	
	
	for(int i= 0; i < n; i++){
		for(int j = 0; j  < n; j++){
			printf("%3d ", arr[i][j]);	
		}
		printf("\n");
	}
	
	return 0;
}
{% endhighlight %}


