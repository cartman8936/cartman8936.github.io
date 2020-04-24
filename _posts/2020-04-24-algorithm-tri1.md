---
layout: post
title:  "삼각형 출력 1"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
첫 번째 줄에 10 이하의 자연수 N이 입력된다.


▣ 입력설명 

첫 번째 줄에 자연수 N이 입력된다.

▣ 출력설명 

아래와 같은 모양을 출력한다.


▣ 입력 예제 1
```
3
```

▣ 출력 예제 1
```
@@@
@@
@

```
▣ 입력 예제 2
```
5
```

▣ 출력 예제 2
```
@@@@@
@@@@
@@@
@@
@

```

### Solution

{% highlight cpp %}
#include<stdio.h>
int main(){
	int a;
	scanf("%d", &a);
	
	for(int i = 0; i < a; i++){
		for(int j = a ; j > i; j--){
			printf("@");	
	    }
		printf("\n");
	}
	return 0;
}
{% endhighlight %}


