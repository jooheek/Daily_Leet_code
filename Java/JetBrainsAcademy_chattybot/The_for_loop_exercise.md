### Task : find the roots of a cubic equation

- ax^3+bx^2+cx+d=0 함수를 만족하는 해를 구하라 
- 0에서 1000 사이

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

- 왜인지는 모르겠지만 2부터 5등급으로 점수를 매긴다
- 5-> A, 4->B, 3->C, 2->D
-학생수는 n명

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

- 뭔 문제가 이렇지 
- 숫자 두개를 입력한다. ex) input : 8,15 ouptput :  8 Fizz Buzz 11 Fizz ... 15
- 3의 배수일때는 Fizz 5의 배수일때는 Buzz 3과5의 배수일때는 FizzBuzz
- 둘다로 안나눠질때는 숫자그대로 나옴

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

- output : 숫자 두개
- 두 숫자 사이에서 3으로 나눠지는 모든 수의 평균 ex)input :-5,12  -3 ,0,3,6,9,12 output: 4.5

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
- 첫번째 숫자가 그 다음에 오는 숫자들의 총 갯수 
- 6의 배수인 숫자들의 총 합을 구하라

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

- 숫자 세개 a,b,n이 있다 a이상 b이하의 숫자중 n으로 나눠지는 수의 갯수를 구하라

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
- long형의 양수 m를 입력하면 n!>m 을 만족하는 n을 구하라

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

