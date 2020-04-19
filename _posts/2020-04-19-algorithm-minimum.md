---
layout: post
title:  "연필 갯수"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
100이하의 자연수 A, B, C를 입력받아 세 수 중 가장 작은 값을 출력하는 프로그램을 작성하세요.



▣ 입력설명 

첫 번째 줄에 1000 이하의 자연수 N이 입력 된다.

▣ 출력설명 

첫 번째 줄에 가장 작은 수를 출력한다.


▣ 입출력 예제 1

6 5 11 / 5

▣ 입출력 예제 2

13 25 17 / 13


▣ 입출력 예제 3

19 23 11 / 11

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
    int a, b ,c;
    scanf("%d %d %d", &a, &b, &c);
	int min;
	if(a<b){
		min = a;
	}else{
		min = b;
	}
	
	if(c<min){
		min = c;
	}
		
    printf("%d", min);
    return 0;
}
{% endhighlight %}


