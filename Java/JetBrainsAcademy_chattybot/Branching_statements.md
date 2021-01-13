
### Task : The break statement

- break��  �ܺ��� loop�� ������ ���Ѵ�.

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

- for loop������ continue�� ����,���ҹ����� �̵��Ѵ�.
- while,do - while������ continue�� �ٷ� ���ǹ����� �̵��Ѵ�.
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

- 0���� ������ ������ ������ �ִ�. ¦���� even, Ȧ���� odd�� ����϶�(�� 0�� ����) 

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

- ���ڸ� ���̾� �ִ´�. ���� 0�� ������ �������� ��� ���� �ջ��� ���´�. ���� �� ���� 1000�̻��̸� �� -1000 �� ���´�.

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

- ������ ����, ������ �ٸ��� ������ ����, �� �ٸ��� ���̸� �޴´�.
- ������ ���̰� �ٸ��� ���̺��� ���� ���  ������ �� ������ ���� ��� �ٸ��� �浹�ϰԵȴ�.
-  ���� �浹�Ѵٸ� ���° �ٸ��� �浹�ϴ��� ���ϰ� �浹���� �ʴ´ٸ� �浹���� �ʴ´ٴ� ������ ����϶�.

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

- �迭�� �ٸ��� ���̸� �������� �ʰ� �浹�� ��� �ٷ� ������ ��µǴ� ���� 
- System.exit(0) �� �������� �� ���� ���ڴ� ������ ������ �����.

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
- print ������ ���׿����� ����غ� ��
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
- do while���� ���ǿ� ���� �ʴ� �����͵�  ����ȴ�.

```
        int input;
        do {
            input = scanner.nextInt();
            nums.add(input);
        } while (input != 0);
```

-  while ���� ����� ���� input�� �ٽ� �����ؾ��Ѵ�.
```	
        int input =scanner.nextInt();
        while (input != 0) {
            nums.add(input);
            input = scanner.nextInt();
        }
```
