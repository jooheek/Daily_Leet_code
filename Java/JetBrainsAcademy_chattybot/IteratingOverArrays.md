### Task : Sum array elements greater than a value

- 배열의 크기, 배열의 요소, output의 기준이 되는 barrier가 차례로 입력된다.
- barrier 를 초과하는 배열들의 합을 구하라. 

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
       Scanner scanner = new Scanner(System.in);
       int size = scanner.nextInt();
       int arr[] = new int[size];
       int sum =0;

       for(int i = 0; i < size ; i++){
           int a = scanner.nextInt();
           arr[i] = a;
       }
       int barrier = scanner.nextInt();

       for(int a = 0; a < size; a++){
           if(arr[a] > barrier){
               sum += arr[a];
           }
       }
        System.out.println(sum);
    }
}
```

- for -each문 적용해 볼것.
```
for (int i : array) {
            if (i >barrier) {
                sum += i;
            }
        }
```
------

### Task : The index of the first max in an array

- 배열의 크기, 각 배열의 요소 가 입력된다.
- 배열에서 가장 큰 요소의 첫번째 인덱스를 구하라.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
       Scanner scanner = new Scanner(System.in);
       int size = scanner.nextInt();
       int arr[] = new int[size];
       int max =0;
       int maxIndex=0;

       for(int i = 0; i < size ; i++){
           int a = scanner.nextInt();
           arr[i] = a;
       }
        for(int i = 0; i < size ; i++){
            if(arr[i]>max){
                max = arr[i];
                maxIndex =i;
            }
        }System.out.println(maxIndex);
    }
}
```
- max 를 정의하지않고  배열끼리 비교해서 index를 구하는 방법도 있다.

```
        int index = 0;
        for (int i = 0; i < size; i++) {
            if (arr[i] > arr[index]) {
                index = i;
            }
        }
```

------

### Task :

- 

```
```

------

### Task :

- 

```
```

------

### Task :

- 

```
```
