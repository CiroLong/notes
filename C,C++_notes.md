# C语言笔记

## ANSI码表

![enm7ku7y](E:\笔记\enm7ku7y.png)

## 简单的C代码

```c
#include<stdio.h>//包含一个头文件
int main()//主调函数
{
    printf("Hello,world!");
    
    return 0;
}
```

## 链接

### `static`的作用

>`static`声明的变量为“文件作用域，内部链接”
>
>所有未加 `static` 前缀的全局变量和函数都具有全局可见性，其它的源文件也能访问。
>如果加了 `static`，就会对其它源文件隐藏。例如在 a 和 msg 的定义前加上 static，main.c 就看不到它们了。利用这一特性可以在不同的文件中定义同名函数和同名变量，而不必担心命名冲突。
>
>不加声明时为“文件作用域，外部链接“（相当于`auto`）

## 储存期

