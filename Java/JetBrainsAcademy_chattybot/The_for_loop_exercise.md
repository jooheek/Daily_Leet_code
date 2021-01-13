### Task : find the roots of a cubic equation

- ax^3+bx^2+cx+d=0 �Լ��� �����ϴ� �ظ� ���϶� 
- 0���� 1000 ����

<pre>
<code>
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        int c = scanner.nextInt();
        int d = scanner.nextInt();

        
        for(int i = 0; i<=1000 ; i++){
            if(a*i*i*i+b*i*i+c*i+d == 0){
                System.out.println(i);
            }
        }
    }
}
</code>
</pre>

---------------------------------------

### Grades

- �������� �𸣰����� 2���� 5������� ������ �ű��
- 5-> A, 4->B, 3->C, 2->D
-�л����� n��

<pre>
<code>
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int As = 0;
        int Bs = 0;
        int Cs = 0;
        int Ds = 0;
        int gradesNum = scanner.nextInt();
        for(int i=0;i<gradesNum;i++){
            switch(scanner.nextInt()){
                case 2:Ds++;
                break;
                case 3:Cs++;
                break;
                case 4:Bs++;
                break;
                case 5:As++;
                break;
                default:
                    break;
            }
        }
        System.out.println(Ds+" "+Cs+" "+Bs+" "+As);
    }
}
</code>
</pre>

---------------------------------------

### Fizz Buzz

- �� ������ �̷��� 
- ���� �ΰ��� �Է��Ѵ�. ex) input : 8,15 ouptput :  8 Fizz Buzz 11 Fizz ... 15
- 3�� ����϶��� Fizz 5�� ����϶��� Buzz 3��5�� ����϶��� FizzBuzz
- �Ѵٷ� �ȳ��������� ���ڱ״�� ����

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();

        for(int i=num1 ;i<=num2;i++){
            if(i%3 ==0 && i%5==0){
                System.out.println("FizzBuzz");
            }else if(i % 5 ==0){
                System.out.println("Buzz");
            }else if(i%3 ==0){
                System.out.println("Fizz");
            }else{
                System.out.println(i);
            }
        }
    }
}
```
---------------------------------------

### Arithmetic average

- output : ���� �ΰ�
- �� ���� ���̿��� 3���� �������� ��� ���� ��� ex)input :-5,12  -3 ,0,3,6,9,12 output: 4.5

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();
        int sum =0;
        int count =0;

        for(int i=num1;i<=num2;i++){
            if(i%3 == 0){
                sum = sum+i;
                count = count +1;
            }
        }
        System.out.println(sum/(double)count);
    }
}
```


----------------------

###  Numbers divisible by six
- ù��° ���ڰ� �� ������ ���� ���ڵ��� �� ���� 
- 6�� ����� ���ڵ��� �� ���� ���϶�

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num1 = scanner.nextInt();
        int sum =0;
        int value;

        for(int i =0;i<num1;++i){
            value = scanner.nextInt();
            sum = value % 6 ==0? sum + value : sum;
        }
        System.out.println(sum);
    }
}
```

--------------------------

### The count of numbers divisible by N

- ���� ���� a,b,n�� �ִ� a�̻� b������ ������ n���� �������� ���� ������ ���϶�

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();
        int num3 = scanner.nextInt();
        int count = 0;
        int sum = 0;
        for(int a = num1;a<=num2;a++){
            if(a % num3 == 0){
                 count = count +1;
            }
        }
        System.out.println(count);
    }
}
```

------------------

###Task : The smallest value
- long���� ��� m�� �Է��ϸ� n!>m �� �����ϴ� n�� ���϶�

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Long a = scanner.nextLong();
        int i=1;
        for(;i<=a;i++){
            a = a/i;

        }System.out.println(i);
    }
}
```

