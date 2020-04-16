---
layout: post
title:  "음료수 자판기"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
자판기에 투입한 금액과 음료수 값이 입력되면 거스름돈과 거스름돈으로 500원의 개수와 100원의 개수를 출력하는 프로그램을 작성하 세요. 자판기의 거스름돈은 500원과 100원만 으로 구성되며, 최소의 개수로 거슬러 주어야 한다.(기본단위는 100원입니다.)

▣ 입력설명 

첫 번째 줄에 자판기에 투입한 금액(10,000 원 이하)이 입력된다. 두 번째 줄에 음료수의 값이 입력된다.

▣ 출력설명 

첫 번째 줄에 거스름돈이 출력된다. 두 번째 줄에 거스름돈을 구성하는 500원의 개수가 출력된다. 세 번째 줄에 거스름돈을 구성하는 100원의 개수를 출력한다

▣ 입출력예제 1

3000 2300 / 700 1 2

▣ 입출력예제 2

5000 2500 / 2500 5 0

▣ 입출력예제 3

8000 5200 / 2800 5 3

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	int a, b;
	scanf("%d %d", &a, &b);
	int change = a - b;
	int res = change;
	int n500 = res / 500;
	res = res - 500 * n500;
	int n100 = res / 100;
	
	printf("%d %d %d", change, n500, n100);
	return 0;
}
{% endhighlight %}


