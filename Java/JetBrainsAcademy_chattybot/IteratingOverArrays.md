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

### Task : Check the sum

- a,b,c 입력값을 준다 셋중 둘을 합해서 정확히 20 이 된다면 true, 아니라면 false

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
- 이런식으로 먼저 정의하지 않는 방법도 있다

```
	boolean result = a + b == 20 || b + c == 20 || c + a == 20;
	System.out.println(result);
```

------

### Task : Check if an array contains two numbers

- 
- Arrays.equal(a,b) 사용함. 배열 a와 b가 같은지 확인한다.

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

        //기존 배열을 두개로 잘라서 비교하기
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
- 조건문을 요소 별로 비교할 수있다.
```
arr[i - 1] == n && arr[i] == m ||   arr[i - 1] == m && arr[i] == n
```

------
