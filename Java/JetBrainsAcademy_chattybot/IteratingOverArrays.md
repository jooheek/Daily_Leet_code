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

### Task : Check the sum

- a,b,c �Է°��� �ش� ���� ���� ���ؼ� ��Ȯ�� 20 �� �ȴٸ� true, �ƴ϶�� false

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
       Scanner scanner = new Scanner(System.in);
       int a = scanner.nextInt();
       int b = scanner.nextInt();
       int c = scanner.nextInt();
       boolean isTwenty = false;

        //if there's a pair of them that adds up to exactly 20.
        if(a+b ==20 || a+c ==20 || b+c ==20){
            isTwenty = true;
        }
        System.out.println(isTwenty);
    }
}
```
- �̷������� ���� �������� �ʴ� ����� �ִ�

```
	boolean result = a + b == 20 || b + c == 20 || c + a == 20;
	System.out.println(result);
```

------

### Task : Check if an array contains two numbers

- 
- Arrays.equal(a,b) �����. �迭 a�� b�� ������ Ȯ���Ѵ�.

```
import java.util.Arrays;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
       Scanner scanner = new Scanner(System.in);
       int size = scanner.nextInt();
       int arr[] = new int[size];
       boolean same = false;

       for(int i =0;i<size;i++){
            arr[i] = scanner.nextInt();
       }

       int n = scanner.nextInt();
       int m = scanner.nextInt();
       int checkArrOne[] = {n,m};
       int checkArrTwo[] = {m,n};

        //���� �迭�� �ΰ��� �߶� ���ϱ�
        for(int i=0; i<arr.length-1;i++){
            int b[] = Arrays.copyOfRange(arr,i,i+2);
           // System.out.println("b :"+b[0]+b[1]);
            if(Arrays.equals(b,checkArrOne) ||Arrays.equals(b,checkArrTwo)){
                same = true;
                break;
            }
        }
        System.out.println(same);
    }
}
```
- ���ǹ��� ��� ���� ���� ���ִ�.
```
arr[i - 1] == n && arr[i] == m ||   arr[i - 1] == m && arr[i] == n
```

------
