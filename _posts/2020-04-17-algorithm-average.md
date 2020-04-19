---
layout: post
title:  "세 수의 평균"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
자연수 A, B, C를 입력받아 세 수의 평균을 구하는 프로그램을 작성하세요. 
출력하는 평균값은 소수 셋 째 자리에서 반 올림하여 출력합니다. 
%0.2f를 사용하면 안 됩니다.


▣ 입력설명 

첫 번째 줄에 100이하의 세 자연수가 입력된다.


▣ 출력설명 

첫 번째 줄에 소수 셋 째 자리에서 반올림한 값을 출력한다.


▣ 입출력 예제 1

5 7 11 / 7.670000

▣ 입출력 예제 2

13 25 17 / 18.330000

▣ 입출력 예제 3

11 19 23 / 17.670000

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	int a, b, c;
	scanf("%d %d %d", &a, &b, &c);
	
	double res =  int ((a + b + c) / 3.0 * 100 + 0.5) / 100.0;
	printf("%lf", res);
	return 0;
}
{% endhighlight %}


