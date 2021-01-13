
### Task : The break statement

- break는  외부의 loop를 멈추지 못한다.

```
class Main {
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            for (int j = 0; j < 10; j++) {
                System.out.print(j + " ");
                if (i == j) {
                    break;
                }
            }
            System.out.println();
        }
    }
}

```
-------

### Task :The continue statement

- for loop문에서 continue는 증가,감소문으로 이동한다.
- while,do - while문에서 continue는 바로 조건문으로 이동한다.
- continue = pass

```
class Main {
    public static void main(String[] args) {
        int n = 10;
        for (int i = 0; i < n; i++) {
            if (i % 2 != 0) {
                continue;
            }
            System.out.print(i + " ");
        }
    }
}
``` 

```
class Main {
    public static void main(String[] args) {
        int n = 10;
        for (int i = 0; i < n; i++) {
            if (i % 2 == 0) {
                System.out.print(i + " ");
            }
        }
    }
}
```

```
class Main {
    public static void main(String[] args) {
        int i =0;
        do{
            if (i % 2 == 0) {
                System.out.print(i + " ");
            }
            i++;
	continue;
        }while(i !=10);
    }
}

```
---------

### Task : Even or odd

- 0으로 끝나는 숫자의 연속이 있다. 짝수면 even, 홀수면 odd를 출력하라(단 0은 제외) 

```
import java.util.ArrayList;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        ArrayList<String> values = new ArrayList<>();
        int a = scanner.nextInt();

        while (a != 0) {
            values.add(a % 2 == 0 ? "even" : "odd");
            a = scanner.nextInt();
        }
        values.forEach(System.out::println);
    }
}
```
---------

### Task : The integer barrier

- 숫자를 연이어 넣는다. 만약 0이 나오면 이전까지 모든 수의 합산이 나온다. 만약 그 수가 1000이상이면 수 -1000 이 나온다.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a;
        int sum = 0;

        while ((a = scanner.nextInt()) != 0) {
            sum += a;
            if (sum >= 1000) {
                sum -= 1000;
                break;
            }
        }
        System.out.println(sum);
    }
}
```

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int sum = 0;
        int n;
        while (scanner.hasNext()) {
            n = scanner.nextInt();
            if (n == 0) {
                System.out.println(sum);
                break;
            }
            sum += n;
            if (sum >= 1000) {
                System.out.println(sum - 1000);
                break;
            }
        }
    }
}
```

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int number = scanner.nextInt();
        int sum = 0;
        int barrier = 1000;

        while (number != 0) {
            sum += number;
            if (sum >= barrier) {
                sum -= barrier;
                break;
            }
            number = scanner.nextInt();
        }
        System.out.print(sum);
    }
}
```

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int sum = 0;
        int input;

        do {
            input = scanner.nextInt();
            sum += input;
        } while (sum < 1000 && input != 0);

        System.out.println(sum >= 1000 ? sum - 1000 : sum);
    }
}
```
-----------

### Task : Bus Tour 

- 버스의 높이, 지나갈 다리의 높이의 갯수, 각 다리의 높이를 받는다.
- 버스의 높이가 다리의 높이보다 낮을 경우  지나갈 수 있지만 높을 경우 다리에 충돌하게된다.
-  만약 충돌한다면 몇번째 다리에 충돌하는지 구하고 충돌하지 않는다면 충돌하지 않는다는 문장을 출력하라.

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int heightOfTheBus = scanner.nextInt();
        int numberOfTheBridges = scanner.nextInt();
        int busInfo[] = new int[numberOfTheBridges+1];
        boolean pass = false;

        for(int i=0; i<numberOfTheBridges;i++){
            busInfo[i] = scanner.nextInt();
        }
        for(int j=0; j<numberOfTheBridges;j++){
            if(heightOfTheBus< busInfo[j]){
                pass =true;
                continue;
            }else {
                System.out.println("Will crash on bridge " + (j+1));
                pass = false;
                break;
            }
        }
        if(pass == true){
            System.out.println("Will not crash");
        }
    }
}

``` 

- 배열에 다리의 높이를 저장하지 않고 충돌할 경우 바로 구문이 출력되는 형태 
- System.exit(0) 는 정상종료 그 외의 숫자는 비정상 종료라고 여긴다.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        int heightOfBus = scanner.nextInt();
        int numOfBridges = scanner.nextInt();

        for (int i = 1; i <= numOfBridges; i++) {
            int heightOfBridge = scanner.nextInt();

            if (heightOfBridge <= heightOfBus) {
                System.out.print("Will crash on bridge " + i);
                System.exit(0);
            }
        }
        System.out.print("Will not crash");
    }
}
```
- print 구문에 삼항연산자 사용해볼 것
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int heightOfTheBus = scanner.nextInt();
        int numOfTheBridge = scanner.nextInt();
        boolean crash = false;
        int heightOfTheBridge;

        for (int i = 1; i <= numOfTheBridge; ++i) {
            heightOfTheBridge = scanner.nextInt();
            if (heightOfTheBridge <=heightOfTheBus) {
                System.out.println("Will crash on bridge " + i);
                crash = true;
                break;
            }
        }
        System.out.println(crash ? "" : "Will not crash");
    }
}
```

-----------------
- do while문은 조건에 맞지 않는 데이터도  시행된다.

```
        int input;
        do {
            input = scanner.nextInt();
            nums.add(input);
        } while (input != 0);
```

-  while 문을 사용할 때는 input을 다시 정의해야한다.
```	
        int input =scanner.nextInt();
        while (input != 0) {
            nums.add(input);
            input = scanner.nextInt();
        }
```
