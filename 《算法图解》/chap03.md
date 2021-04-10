[toc]
# 递归

## 重要的条件

- 基线条件
- 递归条件

## 一个倒计时小程序

```java
public class CountDown {
    public static void main(String[] args) {
        count(5);
    }

    public static void count(int n) {
        
        System.out.println(n + "...");
        
        if (n <= 0) {
            return;
        } else {
            count(n-1);
        }
    }
}
```

```
5...
4...
3...
2...
1...
0...

Process finished with exit code 0
```



## 输出一个数字是所有位

```java
public class ShowEveryOne {
    public static void main(String[] args) {
        show(123);
    }

    public static void show(int n){
        System.out.println(n % 10);
        if (n >= 1) {
            show(n / 10);
        }
    }
}
/**
3
2
1
0
*/
```

```java
public class ShowEveryOne {
    public static void main(String[] args) {
        show(123);
    }

    public static void show(int n){
        if (n >= 1) {
            show(n / 10);
        }
        System.out.println(n % 10);
    }
}
/**
0
1
2
3
*/
```

- 可以观察到因为输出语句的位置不同，分别表现出逆序输出和正序输出。







