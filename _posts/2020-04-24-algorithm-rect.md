---
layout: post
title:  "정사각형 출력"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
10 이하의 자연수 N이 입력되면 N*N의 사각
형을 아래 그림과 같이 출력하는 프로그램을
작성하세요.

▣ 입력설명 

첫 번째 줄에 자연수 N이 입력된다.

▣ 출력설명 

출력예제처럼 출력한다.


▣ 입력 예제 1

5

▣ 출력 예제 1
```
* * * * *
* * * * *
* * * * *
* * * * *
* * * * *
```
▣ 입력 예제 2

3 


▣ 출력 예제 2
```
* * *
* * *
* * *
```

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	int numLoop;
	
	scanf("%d", &numLoop);
	int res = 0;
	for(int i = 0; i < numLoop; i++){
		int numStd, numApp;
		scanf("%d %d", &numStd, &numApp);
		res += numApp % numStd;
	}
	printf("%d", res);
	return 0;
}
{% endhighlight %}


