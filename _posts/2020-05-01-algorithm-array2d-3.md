---
layout: post
title:  " 2차원 배열 출력 3"
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
  1  0  0  0  2
  0  3  0  4  0  
  0  0  5  0  0  
  0  6  0  7  0  
  8  0  0  0  9

```

▣ 입력 예제 2
```
7

```

▣ 출력 예제 2
```
  1  0  0  0  0  0  2  
  0  3  0  0  0  4  0  
  0  0  5  0  6  0  0  
  0  0  0  7  0  0  0  
  0  0  8  0  9  0  0  
  0 10  0  0  0 11  0 
  12  0  0  0  0  0 13

```



### Solution

{% highlight cpp %}
#include<stdio.h>

int arr[10][10];

int main(){
	
	int n;
	scanf("%d", &n);
	int cnt = 1;
	for(int i= 0; i < n; i++){
		for(int j = 0; j  < n ; j++){
			if(j == (n-1-i) || j == i ){
				arr[i][j] = cnt;
				cnt++;
			}
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


