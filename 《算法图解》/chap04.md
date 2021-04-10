[toc]

# 快排

- 递归版本

```java
public class QuickSortDemo {
    public static void main(String[] args) {
        int[] arr = {1, 4, 2, 6, 3, 6, 8, 2, 9, 56, 2, 4, 2, 1, 90};
        quickSort(arr, 0, arr.length - 1);
        System.out.println(Arrays.toString(arr));
    }

    static void quickSort(int[] arr, int low, int high) {
        if (low >= high) {
            return;
        }

        int save = arr[low];
        int i = low;
        int j = high;
        while (i < j) {
            while (arr[j] >= save && i < j) {
                j--;
            }
            while (arr[i] <= save && i < j) {
                i++;
            }
            int t = arr[i];
            arr[i] = arr[j];
            arr[j] = t;
        }
        arr[low] = arr[i];
        arr[i] = save;
        quickSort(arr, low, j - 1);
        quickSort(arr, j + 1, high);
    }
}
```

- 