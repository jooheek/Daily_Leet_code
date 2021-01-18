### Task : Sum array elements greater than a value

- �迭�� ũ��, �迭�� ���, output�� ������ �Ǵ� barrier�� ���ʷ� �Էµȴ�.
- barrier �� �ʰ��ϴ� �迭���� ���� ���϶�. 

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

- for -each�� ������ ����.
```
for (int i : array) {
            if (i >barrier) {
                sum += i;
            }
        }
```
------

### Task : The index of the first max in an array

- �迭�� ũ��, �� �迭�� ��� �� �Էµȴ�.
- �迭���� ���� ū ����� ù��° �ε����� ���϶�.

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
- max �� ���������ʰ�  �迭���� ���ؼ� index�� ���ϴ� ����� �ִ�.

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
