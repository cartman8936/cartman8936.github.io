---
layout: post
title:  "개울 건너기"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
철수는 학교에 가는데 개울을 만났습니다. 개 울은 N개의 돌로 다리를 만들어 놓았습니다. 철수는 돌 다리를 건널때 한 번에 한 칸 또 는 두 칸씩 건너뛰면서 돌다리를 건널 수 있 습니다. 철수가 개울을 건너는 방법은 몇 가 지인지 구하는 프로그램을 작성하세요.

  <img src="/assets/posts/2020-04-30-algorithm-cross-stream.jpg" title="Explation image">


▣ 입력설명 

첫 번째 줄에 돌의 개수 N(3<=N<=20)이 주어진다.


▣ 출력설명 

첫 번째 줄에 건널 수 있는 방법의 수를 출력한다.

▣ 입력 예제 1
```
3

```

▣ 출력 예제 1
```
5

```

▣ 입력 예제 2
```
7

```

▣ 출력 예제 2
```
34

```
▣ 출력 예제 1
```
5

```

▣ 입력 예제 3
```
9

```

▣ 출력 예제 3
```
89

```

### Solution

{% highlight cpp %}
#include<stdio.h>
int arr[101];

int main(){

	int n;
	scanf("%d", &n);
	
	arr[0] = 1;
	arr[1] = 1;
	
	for(int i = 2; i<=n+1; i++){
		arr[i] = arr[i-1] + arr[i-2];
	}
	printf("%d", arr[n+1]);
	
	return 0;
}
{% endhighlight %}


