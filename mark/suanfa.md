# 算法第四版 谢路云

## 第一章 基础

### java基本结构
- 原始数据类型
    - 整数、浮点、、字符、布尔
    - 布尔型bool(boolean)为两种取值 true false,在bool数据里，0 为 false，否则则为 true(除0之外的任何数)
    - false 看作0，true看作 1，二者逻辑运算，按0 1 走
    - 逻辑运算，！>&&>||
    - int-32 bit
    - double-64 bit  IEEE 754
    - char-16 bit（解释：int 32位，double IEEE 754 规则规定64位，char 16位）
- 语句
    - 声明  给定变量名数据类型（int a，double b，取整型数a、浮点型b）
    - 赋值  给变量赋值
          - java中给数组定义空间，使用new 语句
          - 用法为 int[] a=new int[n];
    - 条件  简单改变执行流程
    - 循环  使系统不断执行某些语句
          - break,continue
          - if,while 同c 
    - 调用和返回
- 数组
    - java数组与c不同
    - java定义数组，数组空间在数组名前
    - ![](array.jpg)
    - Java允许两个数组变量名指向同一位置
    - ![](same%20array.jpg)
    - java初始化数组，如不赋值，则默认初始化为0，布尔数组为false
    - ![](inttialization.jpg)
- 静态方法
     - 静态方法是指处理好的函数程序
     -  调用方式同c
     -  一个方法可以存在多个返回语句，但至多有一个返回值，可以返回void（无返回值）
     -  小记外部库,数学函数math，integer、double转化字符串为整形、浮点型数据
     -  系统库 Java.util.array
![](warehouse.jpg)
头文件备注public class + housename，可调用库；调用函数 static void equation()
![](equation.jpg)
![](mathhouse.jpg)
- 字符串
- 标准输入输出
- 数据抽象
    - 数据抽象是指，可以面向对象，创建新的数据类型，进而进行编程
![](java%20frame.jpg)
### 模块化编程——API（应用程序编程接口）
一些常用的库
![](api1.jpg)
![](api2.jpg)
![](api3.jpg)
数据转换
- parseInt(string s) 将string转化为int数据
- toString(int a/double x)将int/double转化为string数据
- parseDouble(string s)将string转化为double数据
![](string.jpg)
输入输出
![](inOut.jpg)