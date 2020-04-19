---
layout: post
title:  "삼각형 판별하기"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
길이가 서로 다른 A, B, C 세 개의 막대 길 이가 주어지면 이 세 막대로 삼각형을 만들 수 있으면 “YES"를 출력하고, 만들 수 없으 면 ”NO"를 출력한다.


▣ 입력설명 

첫 번째 줄에 100이하의 서로 다른 A, B, C 막대의 길이가 주어진다.

▣ 출력설명 

첫 번째 줄에 “YES", "NO"를 출력한다.


▣ 입출력 예제 1

6 7 11 / YES

▣ 입출력 예제 2

13 33 17 / NO


▣ 입출력 예제 3

11 19 23 / YES

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
    int a, b ,c;
    scanf("%d %d %d", &a, &b, &c);
	bool res;
	int max;
	if(a >= b){
		max = a;
		res = (a  < b + c);
	} else {
		max = b;
		res = (b  < a  + c);
	}
	
	if( c >= max){
		max = c;
		res = (c < a + b);
	}

	if(res){
		printf("%s", "YES");
	}else{
		printf("%s", "NO");
	}
	
    return 0;
}
{% endhighlight %}


