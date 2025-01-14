---
title: C语言中qsort用法
categories: 学习
date: 2021-03-09 21:35:43
tags: C语言
---

排序方法有很多种：选择排序，冒泡排序，归并排序，快速排序等。 看名字都知道快速排序是目前公认的一种比较好的排序算法。因为他速度很快，所以系统也在库里实现这个算法，便于我们的使用。 这就是qsort函数(全称quicksort)。它是ANSI C标准中提供的，其声明在stdlib.h文件中，是根据二分法写的，其时间复杂度为n*log(n)

功能： 使用快速排序例程进行排序
头文件：stdlib.h

<!--more-->

用法：  

void qsort(void* base,size_t num,size_t width,int(__cdecl*compare)(const void*,const void*)); 
　　参数： 1 待排序数组，排序之后的结果仍放在这个数组中
　　　　　 2 数组中待排序元素数量
　　　　    3 各元素的占用空间大小（单位为字节）
　　           4 指向函数的指针，用于确定排序的顺序（需要用户自定义一个比较函数）

　　qsort要求提供一个自己定义的比较函数。比较函数使得qsort通用性更好，有了比较函数qsort可以实现对数组、字符串、结构体等结构进行升序或降序排序。


　　如比较函数 int cmp(const void *a, const void *b) 中有两个元素作为参数（参数的格式不能变），返回一个int值，比较函数cmp的作用就是给qsort指明元素的大小是怎么比较的。

### 一、对int类型数组排序

```c
int num[100]; 
int cmp ( const void *a , const void *b ) { 
  return *(int *)a - *(int *)b; 
} 
qsort(num,100,sizeof(num[0]),cmp); 
```

可见，参数列表是两个空指针，现在他要去指向你的数组元素。所以转换为你当前的类型，然后取值。默认升序排列(从小到大)，如果想降序排列返回*b-*a即可。

### 二、对char类型数组排序（同int类型）

```c
char word[100]; 
int cmp( const void *a , const void *b ) { 
	return *(char *)a - *(char *)b; 
} 
qsort(word,100,sizeof(word[0]),cmp); 
```

### 三、对double类型数组排序（特别要注意）

```c
double in[100]; 
int cmp( const void *a , const void *b ) { 
	return *(double *)a > *(double *)b ? 1 : -1; 
} 
qsort(in,100,sizeof(in[0]),cmp);
```

在对浮点或者double型的一定要用三目运算符，因为要是使用像整型那样相减的话，如果是两个很接近的数则可能返回一个很小的小数（大于-1，小于1），而cmp的返回值是int型，因此会将这个小数返回0，系统认为是相等，失去了本来存在的大小关系

### 四、对结构体一级排序

```c
struct In { 
	double data; 
	int other; 
}s[100]；
int cmp( const void *a ,const void *b) { 
	return (*(struct In *)a).data > (*(struct In *)b).data ? 1 : -1; 
} 
qsort(s,100,sizeof(s[0]),cmp); 
```

 ### 五、对结构体二级排序

```c
struct In { 
	int x; 
	int y; 
}s[100]; 
 
//按照x从小到大排序，当x相等时按照y从大到小排序 
int cmp( const void *a , const void *b ) { 
	struct In *c = (struct In *)a; 
	struct In *d = (struct In *)b; 
	if(c->x != d->x) return c->x - d->x; 
	else return d->y - c->y; 
} 
qsort(s,100,sizeof(s[0]),cmp); 
```

### 六、对字符串进行排序 

```c
char word[100][10];
int cmp_string(const void* _a , const void* _b){　　//参数格式固定
    char* a = (char*)_a;　　//强制类型转换
    char* b = (char*)_b;
    return strcmp(a,b);
}

qsort(word,100,sizeof(word[0]),cmp_string);
```