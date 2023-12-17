# C语言习题*50

### 一、程序补全题

1、补全以下函数，要求将a指针和b指针指向的内存空间中存储的值交换。

例如：\*a = 3, \*b = 4，则交换后\*a = 4, \*b = 3。

```cpp
void swap(int *a, int *b) {
    
}
```

2、补全以下函数，要求将字符串数组s中下标为奇数的字符按照其ASCII值从大到小的顺序进行排序。函数参数中s是指向s数组的指针，len表示该字符数组中的元素个数。

例如：原字符串为abcdefg，第一个字符a的下标为0，则排序后字符串变为afcdebg。

```cpp
void sortOddNumber(char *s, int len) {
    
}
```

3、补全以下函数，要求将整数a（a中不包含数字0）反转后作为整型返回。

例如：a = 156，则反转后a = 651

```cpp
int reverse(int a) {
    
}
```

4、补全以下函数，要求用递归的方式计算n的阶乘。

例如：n = 5，返回120

```cpp
int factorial(int n) {
    
}
```

5、补全以下函数，要求将一个仅包含小写字母组成的单词和空格的句子中的所有单词倒置，并通过标准输出打印到屏幕上。函数参数中的len表示字符数组的长度。

例如：原字符串为I am a student，倒置后变为student a am I

```cpp
void reverseSentence(char *s, int len) {
    
}
```

6、补全以下函数，要求将长度为len的字符串s中的k个字符左旋。

例如：ABCD左旋一个字符得到BCDA

​			ABCD左旋两个字符得到CDAB

```cpp
void leftMove(char s[], int len, int k) {
    
}
```

7、补全以下程序，要求从标准输入中读入整形a、b、c，并用a存三个数中的最大值，b次之，c中存最小值。并输出。

```cpp
#include <stdio.h>

int main() {
    int a = 0;
    int b = 0;
    int c = 0;
    scanf("%d %d %d", &a, &b, &c);
    // ...
    printf("%d %d %d\n", a, b, c);
    return 0;
}
```

8、补全以下函数，实现求两个数a和b的最大公约数
```cpp
int gcd(int a, int b) {

}
```

9、以下程序中函数float fun(int n)的功能是：根据下列公式计算并返回s的值(n >= 0)

page 94

```cpp
#include <stdio.h>

float fun(int n) {
    float s = 0.0, w, f = -1.0; int i;
    for (int i = 0; i <= n; i ++) {
        f = _____________; // -f
        w = f / (2 * i + 1);
        _________________; // s += w
    }
    return s;
}

int main() {
    int n = 5; float s;
    __________________; // s = fun(n)
    printf("%f\n", s);
    return 0;
}
```

### 二、填空题

1、写出以下程序运行的输出结果。

```cpp
#include <stdio.h>

int main() {
    int a[3][4] = {0};
    printf("%d\n", sizeof(a)); // 48
    printf("%d\n", sizeof(a[0][0])); // 4
    printf("%d\n", sizeof(a[0])); // 16
    return 0;
}
```

2、写出以下程序运行的输出结果。

```cpp
#include <stdio.h>

int main() {
    int a[3][4] = {0};
    printf("%d\n", sizeof(a[0] + 1)); // 4
    printf("%d\n", sizeof(*(a[0] + 1))); // 4
 	printf("%d\n", sizeof(a + 1)); // 4
    return 0;
}
```

3、写出以下程序运行的输出结果。

```cpp
#include <stdio.h>

int main() {
    int a[3][4] = {0};
    printf("%d\n", sizeof(*(a + 1))); // 16
    printf("%d\n", sizeof(&a[0] + 1)); // 4
    printf("%d\n", sizeof(*(&a[0] + 1))); // 16
    return 0;
}
```

4、写出以下程序运行的输出结果。

```cpp
#include <stdio.h>

int main() {
    int a[3][4] = {0};
    printf("%d\n", sizeof(*a)); // 16
    printf("%d\n", sizeof(a[3])); // 16
    return 0;
}
```

5、写出以下程序运行的输出结果。

```cpp
#include <stdio.h>

struct S1 {
    char c1;
    int a;
    char c2;
};

struct S2 {
    char c1;
    char c2;
    int a;
};

int main() {
    struct S1 s1 = {0};
    printf("%d\n", sizeof(s1)); // 12
    struct S2 s2 = {0};
    printf("%d\n", sizeof(s2)); // 8
    return 0;
}
```

6、写出以下程序的输出结果

```cpp
#include <stdio.h>

struct S3 {
    double d;
    char c;
    int i;
};

int main() {
    printf("%d\n", sizeof(struct S3)); // 16
    return 0;
}
```

7、C程序必须经过<u>编译</u>、<u>链接</u>后生成可执行文件，才能运行。

8、写出以下程序的输出结果

```cpp
#include <stdio.h>

int main() {
    int i = 8, j = 10;
    int m = ++i;
    int n = j ++;
    int x = -i ++;
    int y = j + 12 / ++j;
    printf("%d %d %d %d\n", i, j, m, n); // 10 12 9 10
    printf("%d %d %d %d\n", i, j, x, y); // 10 12 -9 13
    return 0;
}
```

9、若int类型数据占2字节, 则以下语句的输出为：
```cpp
int k = -1;
printf("%d %u\n", k, k);
// -1, 65535
```

10、若a、b、c的值分别为1、0、3, 则执行d = (b ++ && ++a) || c ++后，a、b、c、d的值分别为:
<br>
a = 1, b = 1, c = 4, d = 1

11、除goto语句外，在循环结构中执行<u>continue</u>语句可提前结束本次循环直接进入下一次循环。

12、以下程序运行时，输出到屏幕的结果中第一行是<u>1 1 2</u>, 第二行是<u>3 5 8</u>。
```cpp
#include <stdio.h>

int main() {
    int i, m = 1, n = 1;
    printf("%4d%4d", m, n);
    for (int i = 2; i < 9; i ++) {
        n = n + m;
        m = n - m;
        if (i % 3 == 0)
            printf("\n");
        printf("%4d", n);
    }
    return 0;
}
```
第一行：1 1 2, 第二行：3 5 8

13、以下程序运行后输出结果的第一行是<u>23</u>, 第二行是<u>other</u>

```cpp
#include <stdio.h>

int main() {
    int i, a = 0, c = 2;
    for (i = 0; i < 2; i ++) {
        switch(++ a, a * c) {
            case 1: printf("1");
            case 2: printf("2");
            case 3: printf("3\n"); break;
            default: printf("other\n");
        }
    }
    return 0;
}
```

14、以下程序的输出结果是？（注意静态变量的用法）
```cpp
#include <stdio.h>

int fun(int a) {
    int b = 0;
    static int c = 3;
    b ++, c ++;
    return a + b + c;
}

int main() {
    int i;
    for (int i = 0; i < 3; i ++) {
        printf("%d %d\n", i, fun(5));
    }
    return 0;
}
```
0 10

1 11

2 12

15、以下程序运行时输出到屏幕的结果第一行是<u>5</u>, 第二行是<u>7</u>, 第三行是<u>8</u>

```cpp
#include <stdio.h>

int g(int x, int y) {
    return x + y;
}

int f(int x, int y) {
    {
        static int x = 2;
        if (y > 2) {
            x = x * x; y = x;
        }
        else y = x + 1;
    }
    return x + y;
}

int main() {
    int a = 3;
    printf("%d\n", g(a, 2));
    printf("%d\n", f(a, 3));
    printf("%d\n", f(a, 2));
    return 0;
}
```

16、以下程序运行后输出结果是？
```cpp
#include <stdio.h>

int mystery(int a, int b) {
    if (b == 1) return a;
    else return a + mystery(a, b - 1);
}

int main() {
    int x = 5, y = 3;
    printf("%d\n", mystery(x, y));
    return 0;
}
```

15

### 三、程序设计题

1、定义一个结构体变量(包括年、月、日)，要求输入年月日，计算并输出该日在本年中是第几天。

提示：

1. 定义结构体类型表达日期信息，使用结构体变量来存储输入的日期。
2. 利用switch语句，根据月份以及是否为闰年计算出天数，存在int型变量days中。
3. 用printf函数输出结果

### 四、选择题

1、以下表示数学式"a < b < c"的逻辑表达式中，错误的是（A）
<br>
A. a < b < c
<br>
B. a < b && b < c
<br>
C. !(a >= b) && !(b = c)
<br>
D. a >= b && b >= c

2、以下输出语句中有语法错误的是（A）
<br>
A. printf("%d", 0e);
<br>
B. printf("%d", 0e2);
<br>
C. printf("%d", 0x2);
<br>
D. printf("%s", "0x2");

3、已有声明"int x, a = 3, b = 2;", 则执行赋值语句"x = a > b ++ ? a ++ : b ++;"后，变量x、a、b的值分别为（A）
<br>
A. 3 4 3 
<br>
B. 3 3 4 
<br>
C. 3 3 3 
<br>
D. 4 3 4

4、执行以下程序后的结果是（C）
```cpp
#include <stdio.h>
int main() {
    int x = 3;
    do {
        printf("%d\t", x = x - 3);
    }while(!x);
    return 0;
}
```
A. 输出一个数0
<br>
B. 输出一个数3
<br>
C. 输出两个数0和-3
<br>
D. 无限循环，反复输出数

5、以下选项中，不能表示函数sign(x) = {1(x > 0), 0(x = 0), -1(x < 0)}功能的表达式是（C）
<br>
A. s = (x > 0) ? 1 : (x < 0) ? -1 : 0
<br>
B. s = x < 0 ? -1 : (x > 0 ? 1 : 0)
<br>
C. s = x <= 0 ? -1 : (x == 0 ? 0 : 1)
<br>
D. s = x > 0 ? 1 : x == 0 ? 0 : -1

6、以下函数定义中正确的是（A）

A. double fun(double x, double y) {}

B. double fun(double x; double y) {}

C. double fun(double x, double y); {}

D. double fun(double x, y) {}

7、一个c程序的执行是从(B)

A. 本程序的第一个函数开始，到本程序文件的最后一个函数结束

B. 本程序的main()函数开始，到main()函数结束

C. 本程序的main()函数开始，到本程序文件的最后一个函数结束

D. 本程序的第一个函数开始，到本程序main()函数结束

8、以定义的函数有返回值，则以下关于该函数调用的叙述中错误的是（D）

A. 调用可以作为独立的语句存在

B. 调用可以作为一个函数的实参

C. 调用可以出现在表达式中

D. 调用可以作为一个函数的形参

