### Task : Collatz conjecture

- � ���ڸ� �Է��ص� �ᱹ�� 1�� ������ �Լ��� ������.
- 2�� ����̸� ������, 2�� ����� �ƴϸ� 3�踦 ���ϰ� 1�� ���ϱ⸦ �ݺ��Ѵ�.

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

- �־��� ���ڵ� �� ���� ū 4�� ����� ���� ���϶�.
- 1000�� �̸��� ���ڰ� �־����� � ���� 30000�� ���� ���Ѵ�.

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

- ������ ������ �������� 0 �� ���� �ռ� ���� ��� ���� ���� ���Ѵ�.


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

- ���ӵ� ������ �������� 0 �̰� 0�� ������ ���ڵ��� ���� ū ���� ���϶�

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

- input ���� ����, ���� ���� ������ �����϶�

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

- 0�� �ԷµǱ� ������ �Էµ� ������ ������ ���϶�

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