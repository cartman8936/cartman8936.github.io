---
layout: post
title:  "동물의 수 구하기"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
토끼와 닭의 총 마리수와 총 다리수가 주어 지면 토끼와 닭은 각각 몇 마리인지 출력하 는 프로그램을 작성하세요.

▣ 입력설명 

첫 번째 줄 토끼와 닭의 총 마리수가 주어지 고, 두 번째 줄에 토끼와 닭의 총 다리수가 주어진다. 토끼와 닭은 모두 한 마리 이상 있다.

▣ 출력설명 

첫 번째 줄에 토끼의 수와 닭의 수를 차례로 출력한다.


▣ 입출력 예제 1

10 26 / 3 7

▣ 입출력 예제 2

26 74 / 11 15

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	int a, b;
	scanf("%d %d", &a, &b);
	
	int numRabbit, numChick;	
	
	//i = 토끼의 수 
	for(int i = 0; i < a; i++){
		if(4 * i + 2 * (a-i) == b){
			numRabbit = i;
			numChick = (a - i);
		} 
	}	
	printf("%d %d", numRabbit, numChick);
	
	return 0;
}
{% endhighlight %}


