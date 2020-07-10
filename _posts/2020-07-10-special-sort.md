---
layout: post
title:  "Special Sort(구글 인터뷰)"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
N개의 정수가 입력되면 당신은 입력된 값을 정렬해야 한다.
음의 정수는 앞쪽에 양의정수는 뒷쪽에 있어야 한다. 또한 양의정수와 음의정수의 순서에는
변함이 없어야 한다.


▣ 입력설명 

첫 번째 줄에 정수 N(5<=N<=100)이 주어지고, 그 다음 줄부터 음수를 포함한 정수가 주어진
다. 숫자 0은 입력되지 않는다

▣ 출력설명 

정렬된 결과를 출력한다.


▣ 입력 예제 1
```
8
1 2 3 -3 -2 5 6 -6


```

▣ 출력 예제 1
```
-3 -2 -6 1 2 3 5 6

```

### Solution
{% highlight cpp %}
#include<stdio.h>
int main(){
	freopen("input.txt", "rt", stdin);
	int n;
	scanf("%d", &n);
	
	int arr[100];
	for(int i = 0; i < n; i++){
		scanf("%d", &arr[i]);
	}
	
	for(int i = 0; i < n ; i++){
		int temp = 0;
		for(int j=0; j < n-1-i; j++){
			
			if(arr[j] > 0 && arr[j+1] <0 ){
				temp = arr[j+1];
				arr[j+1] = arr[j];
				arr[j] = temp;
			}
		}
	}
	
	for(int i = 0; i < n; i++){
		printf("%d ", arr[i]);
	}

	return 0;
}




{% endhighlight %}


