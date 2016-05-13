# include语句用法

## include语句的两种语法：
include语句有两种方式包含头文件，分别是使用双引号***""*** 和左右尖括号 ***<>***。其区别是（对于不是使用完全文件路径名的）头文件的搜索顺序不同。

## 使用双引号""的头文件搜索顺序：
* 包含该#include语句的源文件所在目录
* 包含该#include语句的源文件的已经打开的头文件的逆序
* 编译选项-I所指定的目录
* 环境变量INCLUDE所定义的目录

## 使用左右尖括号<>的头文件的搜索顺序：
* 编译选项-I所指定的目录
* 环境变量INCLUDE所定义的目录


## 示例代码：
```c
#include <myheader.h>
#include "myheader.h"

int add(int,int);

int triple(int x)
{
    return add(x, add(x, x));
}
```