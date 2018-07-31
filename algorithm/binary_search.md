# 原理分析
[二分查找](https://www.cnblogs.com/luoxn28/p/5767571.html)
# 代码示例


```c
#include <stdio.h>
// 原始简单版
int BSearch(int a[], int n, int val)
{
    if (n <= 0) {
        return -1;
    }

    int b = 0;
    int e = n - 1;
    int mid = 0;

    while (b <= e) {
        mid = (b+e)/2;
        if (a[mid] == val) {
            return mid;
        } else if (a[mid] > val) {
            e = mid - 1;
        } else {
            b = mid + 1;
        }
    }

    return -1;
}

int main()
{
    int a[7] = {1,3,4,6,8,9,10}; 
    int val = 5;
    int pos = BSearch(a, 7, val);
    if (pos >= 0) {
        printf("Find val[%d] at pos[%d]", val, pos);
    } else {
        printf("Not find val[%d]", val);
    }
}

```

