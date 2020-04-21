---
layout: post
title:  "N의 약수 출력하기"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
자연수 N이 입력되면 N의 약수를 출력하는 프로그램을 작성하세요.


▣ 입력설명 

첫 번째 줄에 50이하의 자연수 N이 입력된다.


▣ 출력설명 

첫 번째 줄에 N의 약수를 출력한다.


▣ 입출력 예제 1

6 / 1 2 3 6

▣ 입출력 예제 2

24 / 1 2 3 4 6 8 12 24


▣ 입출력 예제 3

30 / 1 2 3 5 6 10 15 30

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	int a;
	scanf("%d", &a);
	
	int i = 1;
	while(i <= a){
		if(a % i == 0){
			printf("%d ", i);
		}
		i++;
	}
	return 0;
}
{% endhighlight %}


