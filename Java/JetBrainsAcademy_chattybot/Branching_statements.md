
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
