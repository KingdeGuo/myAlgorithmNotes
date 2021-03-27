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
      public static int bindarySearch(int key, int a[], int lo, int hi) {
          if (lo > hi) {
              return -1;
          }
          int mid = lo + (hi - lo) / 2;
          if (key < a[mid]) {
              return bindarySearch(key, a, lo, mid - 1);
          } else if (key < a[mid]) {
              return bindarySearch(key, a, mid + 1, hi);
          } else {
              return mid;
          } 
      }
  ```

- 颠倒数据元素的顺序

  ```java
  	public static int[] reverseArr(int[] a) {
          for (int i = 0; i < a.length / 2; i++) {
              int temp = a[i];
              a[i] = a[a.length - 1 - i];
              a[a.length - 1 - i] = temp;
          }
          return a;
      }
  ```

- 判断一个数是否为素数

  ```java
      public static boolean isPrime(int n) {
          if (n < 2) {
              return false;
          }
          for (int i = 0; i * i < n; i++) {
              if (n % i == 0) {
                  return false;
              }
          }
          return true;
      }
  ```

- 计算平方根（牛顿迭代法）

  ```java
      public static double sqrt(double n) {
          if (n < 0) {
              return Double.NaN;
          }
          double err = 1e-5;
          double t = n;
          while (Math.abs(t - t / n) > err * t) {
              t = (n / t + t) / 2.0;
          }
          return t;
      }
  ```

- 