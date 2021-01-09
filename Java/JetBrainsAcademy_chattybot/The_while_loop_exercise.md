### Task : Collatz conjecture

- 어떤 숫자를 입력해도 결국엔 1이 나오는 함수를 만들어라.
- 2의 배수이면 반으로, 2의 배수가 아니면 3배를 곱하고 1을 더하기를 반복한다.

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        while(a != 1){
            System.out.println(a);
            if(a%2==0){
                a= a/2;
            }else{
                a = a*3+1;
            }
        }
        System.out.println(a);
    }
}
```

### Task : The sequence 

- 주어진 숫자들 중 가장 큰 4의 배수인 수를 구하라.
- 1000개 미만의 숫자가 주어지며 어떤 수도 30000을 넘지 못한다.

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int biggestNum = 0;

        while(scanner.hasNextInt()){
            int a=scanner.nextInt();
            if(a % 4 == 0 && a > biggestNum){
                biggestNum = a;
            }
        }
        System.out.println(biggestNum);
    }
}

```

### Task : The sum of elements

- 나열된 숫자의 마지막에 0 이 오면 앞서 나온 모든 수의 합을 구한다.


```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int sum = 0;
        int number;
        do{
            number = scanner.nextInt();
            sum+=number;
        }while (number!=0);
        System.out.println(sum);
    }
}
```


### Task : The largest element of a sequence

- 연속된 숫자의 마지막은 0 이고 0을 제외한 숫자들의 가장 큰 수를 구하라

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int biggestNUM=0;
        int number;
        do{
            number = scanner.nextInt();
            if(number>biggestNUM){
                biggestNUM = number;
            }
        }while(number!=0);
        System.out.println(biggestNUM);
    }
}
```

### Task :  Squares of natural numbers

- input 보다 작은, 숫자 들의 제곱을 나열하라

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int input = scanner.nextInt();
        int i=1;
        do{
            for(i =1; i*i<=input;i++){
                System.out.println(i*i);
            }
        }while(input  > i*i);
    }
}
```

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int i =1;
        while(i*i<=n){
            System.out.println(i*i);
            ++i;
        }
    }
}
```

### Task : The length of the sequence

- 0이 입력되기 전까지 입력된 수들의 갯수를 구하라

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int count =0;
        int number;
        do{
            number=scanner.nextInt();
            ++count;
        }while (number!=0);
        System.out.println(count-1);
    }
}
```