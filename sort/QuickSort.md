```java
public class QuickSort {
    public static void main(String[] args) {
        int[] arr = {5, 1, 4, 11, 2, 22, 1, 33, 44, 1, 0, -1, 11};

        QuickSort sort = new QuickSort();
        sort.sort(arr, 0, arr.length - 1);

        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i]);
        }
    }


    public void sort(int[] arr, int left, int right) {
        if (left < right) {
            int pivot = partition(arr, left, right);
            sort(arr, left, pivot - 1);
            sort(arr, pivot + 1, right);
        }
    }

    public int partition(int[] arr, int left, int right) {
        int midValue = arr[left];
        int i = left, j = right + 1;

        while (true) {

            do {
                i++;
            } while (i <= right && arr[i] < midValue);

            do {
                j--;
            } while (j >= 0 && arr[j] > midValue);

            if (i >= j) {
                break;
            }
            swap(arr, i, j);
        }

        swap(arr, left, j);

        return j;
    }

    public void swap(int[] arr, int left, int right) {
        int tmp = arr[left];
        arr[left] = arr[right];
        arr[right] = tmp;
    }
}
```

