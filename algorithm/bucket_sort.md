# 特点

* 桶排序对待排序数据的要求必须在某个指定的范围内
* 可以用来排序浮点数，与计数排序和基数排序不同
* 桶排序中，不同的映射函数f\(x\)可以处理不同类型的数据，f\(x\)作用是把原数据映射到桶中。
* 桶排序是稳定的
* 速度快，但是耗空间

# 原理分析

[桶排序分析](
https://www.cnblogs.com/ECJTUACM-873284962/p/6935506.html\
)

# 代码示例

```c
#include <stdio.h>

// 本文示例以浮点数排序为例，所以f(x)=x*10
void bucket_sort(double a[], int n)
{
    if (n <= 1) {
        return;
    }
    double b[10][10];
    int count[10];

    for (int i = 0; i < 10; i++) {
        count[i] = 0;
    }

    for (int i = 0; i < n; i++) {
        int index = (int)(a[i] * 10);
        b[index][count[index]] = a[i];
        int j = count[index]++;

        while (j>0 && b[index][j-1] > a[i]) {
            b[index][j] = b[index][j-1];
            j--;
        }
        b[index][j] = a[i];
    }

    int k = 0;
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < count[i]; j++) {
            a[k++] = b[i][j];
        }
    }
}

void print(double a[], int n)
{
    for (int i = 0; i < n; i++) {
        printf("%.2f\t", a[i]);
    }
    printf("\n");
}

int main()
{
    double a[7] = {0.31,0.39,0.2,0.6,0.44,0.81,0.18};
    print(a, 7);
    bucket_sort(a, 7);
    print(a, 7);
}
```



