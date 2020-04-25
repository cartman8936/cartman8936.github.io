---
layout: post
title:  "주사위 합"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
정육면체 주사위에는 각 면에 1부터 6까지의 자연수가 적혀있다. 두 사위 2개를 던져 나온 눈의 합이 K가 되 는 경우의 수를 출력하는 프로그램을 작성하세요.

▣ 입력설명 

첫 번째 줄에 자연수 K(2<=K<=36)가 주어진다.

▣ 출력설명 

아래와 같은 모양을 출력한다.


▣ 입력 예제 1
```
6
```

▣ 출력 예제 1
```
1 5 
2 4 
3 3 
4 2 
5 1

```
▣ 입력 예제 2
```
9
```

▣ 출력 예제 2
```
3 6 
4 5 
5 4 
6 3

```

### Solution

{% highlight cpp %}

#include<stdio.h>

int main(){
	int a;
	scanf("%d", &a);
	
	for(int i = 1; i <= 6; i++){
		for(int j = 1; j <= 6; j++){
			if(i + j == a){
				printf("%d %d\n", i, j);
			}
		}
	}
	return 0;
}

{% endhighlight %}


