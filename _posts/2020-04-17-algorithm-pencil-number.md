---
layout: post
title:  "연필 갯수"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
연필 1 다스는 12자루입니다. 학생 1인당 연 필을 1자루씩 나누어 준다고 할 때 N명이 학 생수를 입력하면 필요한 연필의 다스 수를 계산하는 프로그램을 작성하세요.


▣ 입력설명 

첫 번째 줄에 1000 이하의 자연수 N이 입력 된다.

▣ 출력설명 

첫 번째 줄에 필요한 다스 수를 출력합니다.


▣ 입출력 예제 1

25 / 3

▣ 입출력 예제 2

178 / 15

▣ 입출력 예제 3

192 / 16

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
    int a;
    scanf("%d", &a);
	
	int res = (a + 11) / 12;
    printf("%d", res);
    return 0;
}
{% endhighlight %}


