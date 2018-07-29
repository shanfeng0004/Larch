# 原理分析
[归并排序](https://www.cnblogs.com/skywang12345/p/3602369.html)
# 代码示例


```c
#include <stdio.h>
#include <stdlib.h>

// 合并数组
void merge_array(int a[], int first, int mid, int end, int temp[])
{
    int i = first;
    int j = mid + 1;
    int k = 0;
    while (i <= mid && j <= end) {
        if (a[i] <= a[j]) {
            temp[k++] = a[i++];
        } else {
            temp[k++] = a[j++];
        }
    }

    while (i <= mid) {
        temp[k++] = a[i++];
    }

    while (j <= end) {
        temp[k++] = a[j++];
    }

    for (int s = 0; s < k; s++) {
        a[first+s] = temp[s];
    }
}

// 归并排序，先分段，然后merge
void merge_sort(int a[], int begin, int end, int temp[])
{
    if (begin < end) {
        int mid = (begin + end) / 2;
        merge_sort(a, begin, mid, temp);
        merge_sort(a, mid + 1, end, temp);
        merge_array(a, begin, mid, end, temp);
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
    int *p = (int*)malloc(7*sizeof(int));
    if (p == NULL) {
        return 1;
    }

    int a[7] = {3,9,2,6,4,8,1};
    print(a, 7);
    merge_sort(a, 0, 6, p);
    print(a, 7);

    free(p);

    return 0;
}

```

