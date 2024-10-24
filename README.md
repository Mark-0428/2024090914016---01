# 2024090914016-李雨凡-01
## 1.高级计算机语言与低级计算机语言，各有什么优劣，你更喜欢哪一类计算机语言？
### 1.	高级语言：

	●	优势：

	●	编程效率高，语法更接近自然语言，易于理解和编写代码。

	●	可移植性强，能够在不同的硬件和操作系统上运行，只需进行少量修改或无需修改。

	●	拥有丰富的库和框架，能大大减少开发时间和工作量。

	●	提供了更好的错误检查和调试机制，便于发现和解决问题。

	●	劣势：

	●	执行效率相对较低，因为需要经过编译或解释的过程。

	●	对硬件的直接控制能力较弱。

### 2.	低级语言：

	●	优势：

	●	执行速度快，能够直接操作硬件，对资源的利用效率高。

	●	占用内存少，适合对资源要求苛刻的系统。

	●	可以实现更精细的控制，满足特定的底层需求。

	●	劣势：

	●	编程难度大，语法复杂，学习成本高。

	●	代码可读性差，维护困难。

	●	可移植性差，不同的硬件平台可能需要大量修改代码。
 ### 我更喜欢低级计算机语言，理由如下：

1. 对硬件的直接控制：低级语言能够更直接地与计算机硬件进行交互，从而实现对硬件资源的高效利用和精细控制。

2. 高效性能：通常能生成更高效的机器代码，执行速度快，占用资源少。

3. 底层优化：便于开发者针对特定的硬件架构和性能需求进行底层的优化。

4. 理解计算机原理：有助于深入理解计算机的工作原理和体系结构。

5. 特定场景需求：在一些对性能和资源要求极高的特定领域，如嵌入式系统、操作系统内核等，低级语言是首选。
## 2.尝试解读hello.c中每一行的内容。
### 以下是对这段代码的解读：

1. #include <stdio.h>：这是一个预处理指令，用于包含标准输入输出头文件，以便在后续代码中使用相关的输入输出函数，如 printf 和 scanf 。

2. int main()：这是主函数，是 C 语言程序的入口点。程序从这里开始执行。

3. {}：是在int main()函数中，将多条语句组合成在一块，组成复合语句。 

4. printf("Hello, world!");：这行代码使用 printf 函数输出字符串 "Hello, world!" 到控制台。

5. return 0;：表示主函数正常结束并返回值 0。在 C 语言中，主函数返回 0 通常表示程序正常结束。主函数的返回值可以被操作系统或其他调用程序获取，用于判断程序的执行状态。
## 3.删去该程序的哪一行不会影响运行结果？
### 在这个 C 语言程序中，删除 return 0; 这一行不会影响程序的运行结果。

理由如下：

在 C 语言的 main 函数中，如果函数的返回值类型是 int ，那么默认情况下，如果没有明确写 return 语句，程序也会自动返回 0 。所以在这个简单的程序中，只输出了 "Hello, world!" ，return 0; 这一行只是显式地指定了返回值为 0 ，删除它不影响程序的输出结果。
## 4.int类型是计算机存储什么元素的方式？为什么main函数要使用int进行声明/定义？
1. int 类型是计算机存储整数元素的方式。整数包括正整数、负整数和零。
2. main 函数使用 int 进行声明/定义，主要是为了明确函数的返回值类型。在 C 语言中，函数通常需要有一个明确的返回值类型，以便编译器和其他程序能够正确处理和理解函数的执行结果。对于 main 函数，如果返回值为 0 ，通常表示程序正常结束；返回其他值可能表示出现了异常或错误情况。
## 5.请调整上述程序的内容，使其输出内容改为Hello glimmer!并附上运行截图
### 调整后内容如下：
```c
#include <stdio.h>

int main() {
    printf("Hello glimmer!");
    return 0;
}
```
![image](https://github.com/Mark-0428/2024090914016---01/blob/main/e53e6fd79c6bf53809fb58d643ada6cf.png)
## 6.课后题，内容如下：
```c
#include <stdio.h>

int zuidagongyueshu(int m, int n) 
{
    while (n!= 0) 
    {
        int c = n;
        n = m % n;
        m = c;
    }
    return m;
}

int main() 
{
    int m, n;
    printf("请输入第一个整数 m:");
    scanf("%d", &m);
    printf("请输入第二个整数 n:");
    scanf("%d", &n);

    int max = zuidagongyueshu(m, n);
    printf("m 和 n 的最大公约数是: %d\n", max);

    return 0;
}
```
