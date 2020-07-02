---
layout: post
title:  "가장 많이 사용된 자릿수"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
N자리의 자연수가 입력되면 입력된 자연수의 자릿수 중 가장 많이 사용된 숫자를 출력하는 프로그램을 작성하세요.
예를 들어 1230565625라는 자연수가 입력되면 5가 3번 상용되어 가장 많이 사용된 숫자입니다. 
답이 여러 개일 경우 그 중 가장 큰 수를 출력하세요


▣ 입력설명 

첫 줄에 자연수가 입력됩니다. 자연수의 길이는 100을 넘지 않습니다.

▣ 출력설명 

자릿수의 곱을 출력합니다.



▣ 입력 예제 1
```
1230565625

```

▣ 출력 예제 1
```
5

```

### Solution
{% highlight cpp %}
#include <iostream>
int digitArr[10];

int main(){

	char a[101]; 
	scanf("%s", &a);
	
	int digit;
	for(int i = 0; a[i] != '\0'; i++){
		digit = a[i] - 48;
		digitArr[digit]++;
	}

	int maxIdx = 0;
	int max = -1;

	for(int i = 0; i < sizeof(digitArr) / sizeof(int); i++){
		if(digitArr[i] >= max){
			max = digitArr[i];
			maxIdx = i;
		}
	}

	printf("%d\n", maxIdx);

	return 0;
}
{% endhighlight %}


