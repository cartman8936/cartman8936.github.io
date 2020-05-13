---
layout: post
title:  "모두의 약수"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
자연수 N이 입력되면 1부터 N까지의 각 숫자들의 약수의 개수를 출력하는 프로그램을 작성하 세요. 만약 N이 8이 입력된다면 1(1개), 2(2개), 3(2개), 4(3개), 5(2개), 6(4개), 7(2개), 8(4 개) 와 같이 각 숫자의 약수의 개수가 구해집니다. 출력은 다음과 같이 1부터 차례대로 약수의 개수만 출력하면 됩니다. 1 2 2 3 2 4 2 4 와 같이 출력한다.


▣ 입력설명 

첫 번째 줄에 자연수 N(5<=N<=50,000)가 주어진다.

▣ 출력설명 

첫 번째 줄에 1부터 N까지 약수의 개수를 순서대로 출력한다. (제한시간 1초 이내)

▣ 입력 예제 1
```
8

```

▣ 출력 예제 1
```
1 2 2 3 2 4 2 4

```

### Solution
{% highlight cpp %}
#include <iostream>

/* run this program using the console pauser or add your own getch, system("pause") or input loop */
int arr[50001];	
int main(){
//	freopen("input.txt", "rt", stdin);
	int a;
	scanf("%d", &a);
	for(int i = 1; i <= a; i++){
		for(int j = i; j <= a; j+=i){
			arr[j] += 1;			
		}
	}
	
	for(int i = 1; i <= a; i++){
		printf("%d ", arr[i]);
	}
		
	return 0;
}
{% endhighlight %}


