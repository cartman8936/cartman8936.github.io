---
layout: post
title:  "최대 공약수"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
100 이하의 두 자연수 A, B가 입력되면 두 자연수의 최대공약수를 출력하는 프로그램을 작성하세요.



▣ 입력설명 

첫 번째 줄에 100이하의 자연수 A, B가 입력 된다


▣ 출력설명 

첫 번째 줄에 최대공약수를 출력한다.


▣ 입출력 예제 1

24 36 / 12

▣ 입출력 예제 2

56 84 / 28


▣ 입출력 예제 3

58 64 / 2

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	int a, b;
	scanf("%d %d", &a, &b);

	int min;
	if(a<b){
		min = a;
	} else {
		min = b;
	}
	
	int res;
	
	// 결과는 같지만 비효율적.. 
	for(int i = 1; i <= min; i++){
		if(a % i == 0 && b % i == 0){
			res = i;
		}
	}	
	
	// 최대공약수이므로 뒤에서부터 loop 도는 것이 효율적 
	for(int i = min; i >= 1; i--){
		if(a % i == 0 && b % i == 0){
			res = i;
			break;
		}
	}
	
	printf("%d", res);
	return 0;
}
{% endhighlight %}


