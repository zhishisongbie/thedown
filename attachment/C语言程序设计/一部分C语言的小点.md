# 函数间的数据传入传出
## 为什么使用指针而非数组\结构体
以下为例
~~~ c
int test(int a[])
{
  ~
}
int main()
{
  int a[]={~};
  test(a);
}
~~~
1. 在上例中，是将数组a[]传入 test 中
2. 这种传输方法是目标整体的移动
3. 如果我们使用指针
~~~ c
int test(int *a)
{
  ~
}
int main()
{
  int b[]={~};
  int *a=b[];
  test(a);
}
~~~
1. 此时，效果相同，但仅仅传输了指针a 进入test中
2. 这大大减小了传输的工作量

## 形参与实参的数据关系

[[C语言（三）#函数参数和返回|参照源]]
如下例
```c
#include <stdio.h>

void swap(int, int);

int main() {
    int a = 10, b = 20;
    swap(a, b);

    printf("a = %d, b = %d", a, b);   //最后会得到什么结果？
}

void swap(int a, int b){
    int tmp = a;   //这里对a和b的值进行交换
    a = b;
    b = tmp;
}
```
![image-20220623224752943](https://s2.loli.net/2022/06/23/5QbExfHNM76pBOY.png)
实参a与b的值不会交换
+ 在向函数传递参数时，API实际上是将实参复制了一遍（创建值相等的局部变量），不做其他操作
+ ___但是数组不受此限制，我们在函数中修改数组的值，是直接可以生效的___ 

# 暂时还没想好应当归属的位置

## 结构体扩容

remalloc函数扩容
~~~ c
typedef struct text
{
   int *array;
   int Capacity
}
int mian()
{
   int * newArray = realloc(list->array, sizeof(int) * newCapacity);
   //realloc（扩容对象，扩容后大小）
   if(newArray == NULL) return 0;   
    //如果申请失败，那么就确实没办法插入了，只能返回0表示插入失败了
   list->array = newArray;
   list->capacity = newCapacity;
}
~~~
![[数据结构（一）#^text1]]