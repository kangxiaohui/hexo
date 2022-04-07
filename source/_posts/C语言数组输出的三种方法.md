---
title: C语言数组输出的三种方法
categories: 学习
date: 2021-03-09 24:39:43
tags: C语言
---

<!--more-->

### ①下标法

```cpp
#include<stdio.h>
int main(){
	int a[10];
	int i;
	for (i = 0; i<10; i++)
		scanf("%d", &a[i]);
	for (i = 0; i<10; i++)
		printf("%d\n", a[i]);
	printf("\n");
}
```

### ②由数组名计算地址

```cpp
#include<stdio.h>
int main(){
	int a[10];
	int i;
	for (i = 0; i<10; i++)
		scanf("%d", &a[i]);
	printf("\n");
	for (i = 0; i<10; i++)
		printf("%d\n", *(a + i));
	printf("\n");
}
```

### ③用指针变量指向数组元素

```cpp
#include<stdio.h>
int main(){
	int a[10];
	int i, *p;
	for (i = 0; i<10; i++)
		scanf("%d", &a[i]);
	printf("\n");
	for (p = a; p<(a + 10); p++)
		printf("%d", *p);
	printf("\n");

}
```