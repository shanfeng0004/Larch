# 原理分析
[图解堆排序](https://www.cnblogs.com/MOBIN/p/5374217.html)
# 代码示例 


```c
#include <stdio.h>

void adjust(int a[], int pos, int n)
{
    int max = pos;
    int left = 2*pos + 1;
    int right = 2*pos + 2;

    while (left < n || right < n) {
        if (left < n && a[max] < a[left]) {
            max = left;
        }
        if (right < n && a[max] < a[right]) {
            max = right;
        }

        if (max != pos) {
            int temp = a[max];
            a[max] = a[pos];
            a[pos] = temp;

            pos = max;
            left = 2*pos + 1;
            right = 2*pos + 2;
        } else {
            break;
        }
    }
}

void build(int a[], int n)
{
    int pos = n/2 - 1;
    for (int i=pos; i>=0; i--) {
        adjust(a, i, n);
    }
}

void heap_sort(int a[], int n)
{
    build(a, n); 
    int i = n;
    while (i > 1) {
        int tmp = a[i-1];
        a[i-1] = a[0];
        a[0] = tmp;
        i--;
        adjust(a, 0, i); 
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
    heap_sort(a, 7);
    print(a, 7);
}
```

