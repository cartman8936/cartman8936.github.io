---
layout: post
title:  "뒤집은 소수"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
N개의 자연수가 입력되면 각 자연수를 뒤집은 후 그 뒤집은 수가 소수이면 그 수를 출력하는
프로그램을 작성하세요. 예를 들어 32를 뒤집으면 23이고, 23은 소수이다. 그러면 23을 출력
한다. 단 910를 뒤집으면 19로 숫자화 해야 한다. 첫 자리부터의 연속된 0은 무시한다.
뒤집는 함수인 int reverse(int x) 와 소수인지를 확인하는 함수 bool isPrime(int x)를 반드시
작성하여 프로그래밍 한다.



▣ 입력설명 

첫 줄에 자연수의 개수 N(3<=N<=100)이 주어지고, 그 다음 줄에 N개의 자연수가 주어진다.
각 자연수의 크기는 100,000를 넘지 않는다.

▣ 출력설명 

첫 줄에 뒤집은 소수를 출력합니다. 출력순서는 입력된 순서대로 출력합니다.



▣ 입력 예제 1
```
5
32 55 62 3700 250

```

▣ 출력 예제 1
```
23 73

```

### Solution
{% highlight cpp %}
#include <iostream>
#include <iostream>
int digitArr[101];

int reverse(int x){
	int reverse = 0;
	int i = 0;
	while(x > 0){
		i = x % 10;
		// 123 -> 0 + 3 -> 3*10 + 2 -> 32 * 10 + 1
		reverse = reverse * 10 + i;
		x = x / 10;
	}
	
	return reverse;
}

 bool isPrime(int x){
 	if(x == 1) return false;
 	for(int i = 2; i < x / 2 + 1; i++){
 		if(x % i == 0){
 			return false;	
		}
	}
 	return true;
 }


int main(){
	freopen("input.txt", "rt", stdin);

	int a; 
	scanf("%d", &a);
	
	for(int i = 0; i < a; i++){
		scanf("%d", &digitArr[i]);
		if(isPrime(reverse(digitArr[i]))){
			printf("%d ", reverse(digitArr[i]));
		}
	}
	
	return 0;
}
{% endhighlight %}


