---
layout: post
title:  "특정 두자리 수 만들기"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
B < A <10 인 자연수 A, B에 대하여 십의 자리수와 일의 자리수가 각각 A, B인 두 자 리 자연수 중 C 이하의 두 자리 자연수를 모 두 출력하는 프로그램을 작성하세요.
만약 C가 50 이면 위 조건을 만족하는 두 자리 숫자는 21, 31, 32, 41, 42, 43 으로 6개 이다.

▣ 입력설명 

첫 번째 줄에 100 미만의 자연수 C가 입력 된다.

▣ 출력설명 

첫 번째 줄부터 모든 경우의 수를 출력한다. 마지막 줄에 총 개수도 출력한다.

▣ 입력 예제 1
```
50
```

▣ 출력 예제 1
```
21 
31
32
41 
42 
43 
6

```
▣ 입력 예제 2
```
53
```

▣ 출력 예제 2
```
21 
31 
32 
41 
42 
43 
51 
52 
53
9

```

### Solution

{% highlight cpp %}
#include<stdio.h>

int main(){
	int a;
	scanf("%d", &a);
	
	int cnt = 0;
	for(int i = 1; i <= a; i++){
		int secondPos = i / 10;
		int firstPos = i % 10;
		
		if(firstPos != 0 && firstPos < secondPos){
			printf("%d\n",i);
			cnt++;
		}
	}

	printf("%d",cnt);
	
	return 0;
}

{% endhighlight %}


