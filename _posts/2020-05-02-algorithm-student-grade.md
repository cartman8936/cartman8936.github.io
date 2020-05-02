---
layout: post
title:  "성적표"
author: cartman8936
categories: Algorithm
tags:	algorithm c++
cover:  "/assets/instacode.png"
---

### Question
N명의 학생들의 수학, 영어, C언어 점수가 주어지면 수학성적을 1등한 학생의 C언어 점 수를 출력하는 프로그램을 작성하세요.


▣ 입력설명 

첫 번째 줄에 50 이하의 자연수 N이 입력된 다. 그 다음 N줄에 걸쳐 각 학생의 학생번호, 수 학성적, 영어성적, C언어 성적이 차례로 입 력된다. 학생번호를 순서대로 1부터 N이다

▣ 출력설명 

첫 번째 줄에 정답을 출력한다.

▣ 입력 예제 1
```
3 
1 90 80 92 
2 92 93 97 
3 89 90 92

```

▣ 출력 예제 1
```
97

```

### Solution

{% highlight cpp %}
#include<stdio.h>

struct Student{
	int id, math, eng, clang;
};

int maxClang(Student s[], int size){
	int mathMax = -1;
	int maxClang = 0;
	for(int i = 0; i < size; i++){
		if(s[i].math > mathMax){
			mathMax = s[i].math;
			maxClang = s[i].clang;
		}
	}
	return maxClang;
}

int main(){
	int n;
	scanf("%d", &n);
	Student std[n];
	for(int i = 0; i < n; i++){
		scanf("%d",&std[i].id); 	
		scanf("%d",&std[i].math); 	
		scanf("%d",&std[i].eng); 	
		scanf("%d",&std[i].clang); 	
	}	
	printf("%d",maxClang(std, n));
	
	return 0;
}
{% endhighlight %}


