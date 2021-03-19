# 快速排序

## 递归法

```c++
#include<iostream>
using namespace std;
int n,a[1000001];
void qsort(int l,int r)//应用二分思想
{
    int mid=a[(l+r)/2];//中间数
    int i=l,j=r;
    do{
        while(a[i]<mid) i++;//查找左半部分比中间数大的数
        while(a[j]>mid) j--;//查找右半部分比中间数小的数
        if(i<=j)//如果有一组不满足排序条件（左小右大）的数
        {
            swap(a[i],a[j]);//交换
            i++;
            j--;
        }
    }while(i<=j);//这里注意要有=
    if(l<j) qsort(l,j);//递归搜索左半部分
    if(i<r) qsort(i,r);//递归搜索右半部分
}

```

递归中`cmp`的写法

```c
int cmp(a,b){
	if(a > b)return 1;
    else return 0;
}
bool cmp(结构体名称 a，结构体名称 b)
{
    ??
/*判断a是否大于b的代码块，如果a大于或等于b返回1，否则返回否*/
}
```

