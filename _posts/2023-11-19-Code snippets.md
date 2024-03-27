---
title: Code Snippets
author: ge2k
date: 2023-11-19 17:01:20 +0800 
categories: [Blogging, syntax]
tags: [cpp]

---

___
## 2023-11-19

### 片段一
```cpp
#include <bits/stdc++.h>

int main(){
    // int a=1, b=2; 正确 for(int a=1, b=2;;)里面一样可以用

    // int a= b=2; 错误 b未声明

    // int b;
    // int a = b = 2; 声明后可连续赋值
    std::cout << b << '\n';
}

```

### 片段二
```cpp
#include <bits/stdc++.h>

int main(){
    int array[10] = {0}; // array 声明不初始化 内部是随机值
    for (int i : array) std::cout << i;

    std::vector<int> vec(10); // vector 声明不初始化 内部默认0 等价于std::vector<int> vec(10, 0);
    for (int i : vec) std::cout << i << '\n';
}
```

### 片段三
```cpp
#include <bits/stdc++.h>

int main(){
	int i = 10;
	printf("%d %d %d %d %d", i--, --i, ++i, i++, i);//11 10 10 10 10
	// 10 ++i  11 --i 10  i 10 i-- 10 i++ 9
	// 10 ++i  11 --i 10  i-- 10 i++ 9 i 10 
}
```

### 片段四
printf === print formatted 格式化输出
- %c：格式化输出字符
- %s：格式化输出字符串
- %f：格式化输出浮点数
- %e 或 %E：格式化输出科学计数法表示的浮点数
- %o：格式化输出八进制整数
- %d：格式化输出十进制整数
- %x 或 %X：格式化输出十六进制整数
- %u：格式化输出无符号整数
- %lld 或 %llu：格式化输出长长整数（long long int）或无符号长长整数（unsigned long long int）
- %p：格式化输出指针的地址

```cpp
#include <stdio.h>

int main() {
    // 二进制0b 八进制0 十六进制0x
    int bin = 0b1101; // 13 = 1*8+ 1*4+0*2+ 1*1
    printf("The dec number is: %d\n", bin);//13

    int oct = 052; // 42 = 5*8+ 2*1
    printf("The dec number is: %d\n", oct);//42

    // 十六进制数字0-9 A B C D E F
    int hex = 0xe; // 14 = 0*16+ 14*1
    printf("The dec number is: %d\n", hex);//14

    return 0;
}
```

### 片段五
```cpp
// 初始化如果用逗号会共用初始化类型。分号转逗号时避免初始化
ListNode* dummyhead = new ListNode(0); dummyhead->next = head;
```

### 片段六
```cpp
#include <iostream>

int main(){
    int a = 10, cnt =3;
    while(cnt--){
        // 循环的每次迭代都会创建一个新的局部变量 a，并在迭代结束后被销毁
        // 在循环内部创建的局部变量会遮蔽（隐藏）外部具有相同名称的变量。
        // 这意味着在循环内部，访问 a 时，将访问到的是局部变量 a，而不是外部的全局变量 a
        int a = 5;
        std::cout << "local a =" << a << '\n';
    }
    // 循环内部变量a 在循环结束后不会影响全局变量a
    std::cout << "global a =" << a << '\n';
}
```
___