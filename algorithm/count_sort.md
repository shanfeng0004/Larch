# 特点
- 计数排序仅适合于小范围的数据进行排序
- 不能对浮点数进行排序
- 时间复杂度为 O(n)
- 计数排序是稳定的（排序后值相同的元素相对于原先的位置是不会发生变化的）

# 原理分析
[计数排序](https://www.cnblogs.com/developerY/p/3166462.html)
# 代码示例


```c
#include <stdio.h>
//#include <stdlib.h>

void count_sort(int a[], int b[], int n, int k)
{
    if (k <= 1) {
        return;
    }

    // 最大是9的话,则要初始化10个位置,这样才有下标为9的位置
    int c[k+1];
    for (int i = 0; i <= k; i++) {
        c[i] = 0;
    }
    
    for (int i = 0; i < n; i++) {
        c[a[i]]++;
    }

    // 计算数组a中每个元素的位置
    for (int i = 1; i <= k; i++) {
        c[i] += c[i-1];
    }

    for (int j = n-1; j >= 0; j--) {
        int m = a[j];
        int pos = c[m];
        // 位置要减去1才是数组中真正的位置 
        b[pos-1] = m;
        c[m]--;
    }
}

int print(int a[], int n)
{
    for (int i = 0; i < n; i++) {
        printf("%d\t", a[i]);
    }
    printf("\n");
}

int main()
{
    int a[7] = {3,9,2,6,4,8,1};
    int b[7];
    print(a, 7);
    count_sort(a, b, 7, 9);
    print(b, 7);
}

```

