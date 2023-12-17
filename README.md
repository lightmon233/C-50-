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

10、补全函数fun, 其功能是：计算并输出3到n之间所有素数的平方根之而和。

```cpp
#include <stdio.h>
#include <math.h>

double fun(int n) {
    int i, j;
    double s = 0.0;
    for (int i = 3; i <= n; i ++) {
        for (int j = 2; j <= sqrt(i); j ++) {
            if (i % j == 0) {
                break;
            }
        }
        if (j > sqrt(i)) {
            s += sqrt(i);
        }
    }
    return s;
}

int main() {
    printf("%lf\n", fun(5));
    return 0;
}
```

11、不全函数myStrcmp, 实现和c语言库函数strcmp的功能。

```cpp
int myStrcmp(const char *str1, const char *str2) {
    // 放置str1或者str2为空指针
    assert(str1 && str2);
    while (*str1 == *str2) {
        if (*str1 == '\0') {
            return 0;
        }
        str1 ++;
        str2 ++;
    }
    if (*str1 > *str2) return 1;
    else return -1;
}
```

12、完成addPoints函数，使其能够正确地将两个Point相加。

```cpp
#include <stdio.h>

typedef struct {
    int x;
    int y;
} Point;

Point addPoints(Point p1, Point p2);

int main() {
    Point p1 = {2, 3};
    Point p2 = {4, 5};
    Point result = addPpoints(p1, p2);
    printf("Result: (%d, %d)\n", result.x, result.y);
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

17、以下程序运行时，输出结果的第一行是________, 第二行是__________。

```cpp
#include <stdio.h>

void change(int x, int m) {
    char ch[] = {'0', '1', '2', '3', '4', '5', '6', '7', '8', '9'}, b[80];
    int i = 0, r;
    while (x) {
        r = x % m; x /= m; b[i ++] = ch[r];
    }
    for (--i; i >= 0; i --) printf("%c", b[i]);
}

int main() {
    int a, b;
    change(10, 2);
    printf("\n");
    change(10, 8);
    return 0;
}
```

1010

12

18、以下程序的输出结果是__________

```cpp
void swap1(int c[]) {
    int t;
    t = *c; *c = *(c + 1); *(c + 1) = t;
}

void swap2(int a, int b) {
    int t;
    t = a; a = b; b = t;
}

int main() {
    int a[2] = {1, 3}, b[2] = {1, 3};
    swap1(a);
    swap2(b[0], b[1]);
    printf("%2d%2d%2d%2d\n", a[0], a[1], b[0], b[1]);
    return 0;
}
```

3 1 1 3

19、以下程序中函数long fun(char *str)的功能是：自左至右取出非空字符串str中的所有数字字符，将这些数字字符组成一个不超过8位的十进制整数并输出。

例如，字符串str为"efg32gh76.jbejing08t5y4u2", 程序输出：32760854

```cpp
#include <stdio.h>

long fun(char *str) {
    int i = 0; long k = 0;
    char *p = str;
    while (*p != '\0' && __________) {
        if (*p >= '0' && *p <= '9') {
            k = __________ + *p - '0';
            ++i;
        }
        ___________;
    }
    return k;
}

int main() {
    char x[] = "efg32gh76.jbejing08t5y4u2";
    printf("%ld\n", fun(x));
    return 0;
}
```

20、请写出以下程序的输出结果

```cpp
#include <stdio.h>

#define ADD(a, b) a + b

int main() {
    int result = ADD(2, 3) * ADD(4, 5);
    printf("%d\n", result);
    return 0;
}
```

21、以下程序运行时输出的是___________

```cpp
#include <stdio.h>

int f(int n) {
    if (n > 1) return f(n - 2) + n;
    else return n;
}

void main() {
    printf("%d\n", f(8));
}
```

### 三、程序设计题

1、定义一个结构体变量(包括年、月、日)，要求输入年月日，计算并输出该日在本年中是第几天。

提示：

1. 定义结构体类型表达日期信息，使用结构体变量来存储输入的日期。
2. 利用switch语句，根据月份以及是否为闰年计算出天数，存在int型变量days中。
3. 用printf函数输出结果

```cpp
#include <stdio.h>

struct DATE {
    int year;
    int month;
    int day;
};

int main() {
    struct DATE date;
    int days;
    printf("input year-month-day");
    scanf("%d-%d-%d", &date.year, &date.month, &date.day);
    switch (date.month) {
        case 1: days = date.day; break;
        case 2: days = date.day + 32; break;
        case 3: days = date.day + 59; break;
        case 4: days = date.day + 90; break;
        case 5: days = date.day + 120; break;
        case 6: days = date.day + 151; break;
        case 7: days = date.day + 181; break;
        case 8: days = date.day + 212; break;
        case 9: days = date.day + 243; break;
        case 10: days = date.day + 273; break;
        case 11: days = date.day + 304; break;
        case 12: days = date.day + 334; break;
    }
    if ((date.year % 4 == 0 && date.year & 100 != 0 || date.year % 400 == 0) && date.month >= 3)
        days += 1;
    printf("%d-%d-%d is the %dth day in %d.\n", date.year, date.month, date.day, days, date.year);
    return 0;
}
```

2、实现一个单链表，链表初始为空，支持三种操作：

1. 向链表头插入一个数；
2. 删除第 $k$ 个插入的数后面的数；
3. 在第 $k$ 个插入的数后插入一个数。



现在要对该链表进行 $M$ 次操作，进行完所有操作后，从头到尾输出整个链表。

**注意**:题目中第 $k$ 个插入的数并不是指当前链表的第 $k$ 个数。例如操作过程中一共插入了 $n$ 个数，则按照插入的时间顺序，这 $n$ 个数依次为：第 $1$ 个插入的数，第 $2$ 个插入的数，…第 $n$ 个插入的数。

输入格式:

第一行包含整数 $M$，表示操作次数。

接下来 $M$ 行，每行包含一个操作命令，操作命令可能为以下几种：

1. `H x`，表示向链表头插入一个数 $x$。
2. `D k`，表示删除第 $k$ 个插入的数后面的数（当 $k$ 为 $0$ 时，表示删除头结点）。
3. `I k x`，表示在第 $k$ 个插入的数后面插入一个数 $x$（此操作中 $k$ 均大于 $0$）。



输出格式:

共一行，将整个链表从头到尾输出。

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

9、已知有声明"int a[3][3] = {0}, *p1 = a[1], (*p2)[3] = a;", 以下表达式中与"a[1][1] = 1"不等价的表达式是（B）

A. *(p1 + 1) = 1

B. p1[1][1] = 1

C. *(*(p2 + 1) + 1) = 1

D. p2[1][1] = 1

10、以下语句或语句组中，能正确进行字符串赋值的是（D）

A. char *sp; *sp = "right!";

B. char s[10]; s = "right!";

C. char s[10]; *s = "right!";

D. char *sp = "right!";

11、在C语言源程序中，不能用于表示整型常数的数制是（D）

A. 十六进制

B. 八进制

C. 十进制

D. 二进制

12、C语言规定，在一个源程序中main函数的位置（D）

A. 必须在开头

B. 必须在最后

C. 必须在预处理命令的后面

D. 可以在其他函数之前或者之后

13、一个用C语言编写的源程序中，（A）是必不可少的。

A. 取名为main的函数定义 

B. #include <stdio.h>

C. 变量声明

D. 注释

14、以下叙述中正确的是（）

A. 在编译时可以发现注释中的拼写错误

B. C语言程序的每一行只能写一条语句

C. 构成C程序的最小单位是语句

D. C语言程序可以由一个或多个函数组成

15、以下选项中，属于C语言关键字的是（）

A. printf

B. include

C. fun 

D
