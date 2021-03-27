[toc]

# 基础

- 欧几里得算法找最大公约数

  ```java
  public static int getGCD(int p, int q) {
          if (q == 0) {
              return p;
          }
          int r = p % q;
          return getGCD(q, r);
      }
  ```

- 二分查找

  注意被查找数组是有序的

  - 非递归版本

  ```java
  public static int bindarySearch(int a[], int key) {
          int left = 0;
          int right = a.length;
          while (left <= right) {
              int mid = left + (right - left) / 2;
              if (a[mid] == key) {
                  return mid;
              } else if (a[mid] > key) {
                  right = mid;
              } else if (a[mid] < key) {
                  left = mid;
              }
          }
          return -1;
      }
  ```

  - 递归版本

  ```java
  
  ```

- 