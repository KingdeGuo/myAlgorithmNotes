[toc]

# 选择排序

```java
import java.util.Arrays;

public class Demo {
    public static void main(String[] args) {
        int[] arr = new int[]{1, 5, 2, 7, 4, 7, 6, 2, 4, 2, 1};

        for (int i = 0; i < arr.length-1; i++) {
            int index = i;
            for (int j = i + 1; j < arr.length; j++) {
                if (arr[j] < arr[index]) {
                    index = j;
                }
                int t = arr[index];
                arr[index] = arr[i];
                arr[i] = t;
            }
        }

        System.out.println(Arrays.toString(arr));
    }
}
```

