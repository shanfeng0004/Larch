# 原理分析

[图解快速排序](https://www.cnblogs.com/MOBIN/p/4681369.html)

# 代码示例

```c
#include <stdio.h>

int print(int a[], int n);

// 查找pivot
int find_key(int a[], int begin, int end)
{
    int key = a[begin];
    int i = begin;
    int j = end;

    while (i < j) {
        while (i < j && key < a[j]) {
            j--;
        }
        a[i] = a[j];
        while (i < j && a[i] < key) {
            i++;
        }
        a[j] = a[i];
    }
    a[i] = key;
    //printf("begin=%d\tend=%d\ti=%d\ta[begin]=%d\ta[end]=%d\n", begin, end, i, a[begin], a[end]);
    return i;
}

// 快排
int quick_sort(int a[], int begin, int end)
{
    if (begin < end) {
        int key = find_key(a, begin, end);
        quick_sort(a, begin, key-1);
        quick_sort(a, key+1, end);
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
    print(a, 7);
    quick_sort(a, 0, 6);
    print(a, 7);
}
```



