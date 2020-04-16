---
layout: post
title:  "반올림"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
실수값을 입력받아 소수 2째 자리에서 반올 림하는 프로그램을 작성하세요. %0.1f 를 사용하면 안됩니다. 
변수 선언을 double 형으로 해야하고, double a; scanf("%lf", &a)로 입력받는다. 
double 형이 정확하게 나누기 연산을 해준다.

▣ 입력설명 

첫 번째 줄에 소수 둘째 자리에서 반올림한 값을 출력한다.

▣ 출력설명 

첫 번째 줄에 거스름돈이 출력된다. 두 번째 줄에 거스름돈을 구성하는 500원의 개수가 출력된다. 세 번째 줄에 거스름돈을 구성하는 100원의 개수를 출력한다

▣ 입출력예제 1

23.56 / 23.600000

▣ 입출력예제 2

56.77 / 56.800000


▣ 입출력예제 3

76.54 / 76.500000

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	double a;
	scanf("%lf", &a);
	a = a * 100;
	int b = (int)a % 10;

	if(b >= 5){
		a =  a + (10 - b);  
	} else {
		a = a - b;
	}
	
	a = a / 100;
	printf("%lf", a);
	
	return 0;
}

{% endhighlight %}
