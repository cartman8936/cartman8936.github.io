---
layout: post
title:  "삼각형 출력 3"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
10 이하의 홀수인 자연수 N이 입력되면 N크 기의 삼각형을 출력하는 프로그램을 작성하 세요.


▣ 입력설명 

첫 번째 줄에 10 이하의 홀수인 자연수 N이 입력된다

▣ 출력설명 

아래와 같은 모양을 출력한다.


▣ 입력 예제 1
```
5
```

▣ 출력 예제 1
```
  @
 @@ 
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
0 0 0 @
0 0 @ @ 
0 @ @ @ 
@ @ @ @ 
0 @ @ @
0 0 @ @
0 0 0 @

```

### Solution

{% highlight cpp %}

#include<stdio.h>
#include<math.h>

int main(){
	int a;
	scanf("%d", &a);
	int half = a / 2 + 1;
	
	for(int i = 1; i <= a; i++){
		int numBlank = abs(half-i);
		for(int j = 0; j < numBlank; j++){
			printf(" ");
		}
		
		for(int j= numBlank; j < half; j++){
			printf("@");
		}
		
		printf("\n");
	}
	return 0;
}

{% endhighlight %}


