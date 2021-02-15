### Task : Fill the matrix by numbers
- n을 입력받으면 n x n의 형태로 사각형이 그려지고 
![picture of Array](https://postfiles.pstatic.net/MjAyMTAxMjBfMTA2/MDAxNjExMTM2NTgyNjM0.yU8qdB-HK1ZfgmiCv7qpi5b5dD8GjHJDorooD4_Jzvsg.YW1UzLBE7aHe0rfca4gN0dUpAItf2h3C-4IOyvfaFggg.PNG.kimjoohee713/%EB%B0%B0%EC%97%B4.png?type=w966)
- 위의 형태가 된다. 배열을 출력하라.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int cubic[][] = new int [n][n];
        for(int i =0;i<n ;i++){
            for(int j =0;j<n;j++){
                if(Math.abs(i-j)== 0){
                    cubic[i][j] =0;
                }else if(Math.abs(i-j)==1){
                    cubic[i][j] =1;
                }else if(Math.abs(i-j)==2){
                    cubic[i][j] =2;
                }else if(Math.abs(i-j)==3){
                    cubic[i][j] =3;
                }else if(Math.abs(i-j)==4){
                    cubic[i][j] =4;
                }else if(Math.abs(i-j)==5){
                    cubic[i][j] =5;
                }else if(Math.abs(i-j)==6){
                    cubic[i][j] =6;
                }
                System.out.print(cubic[i][j]+" ");
            }
            System.out.println();
        }
    }
}
```
- 배열을 꼭 써야한다는 생각을 버리자.

```

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        for(int i =0;i<n ;i++){
            for(int j =0;j<n;j++){
                System.out.print(Math.abs(i-j)+" ");
            }System.out.println();
        }
    }
}
```
-------

### Task : Rotate a rectangle array
- n X m 배열이 입력된다 이 배열을 시계방향으로 90도 돌린 배열을 출력하라.
-

```

import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int m = scanner.nextInt();
        int cubic[][] = new int [n][m];
        int cubicM[][] = new int[m][n];

        for(int i =0;i<n;i++){
            for(int j =0;j<m;j++){
                cubic[i][j] = scanner.nextInt();
            }
        }
        for(int j =0;j<m;j++){
            for(int i =0;i<n;i++){
                cubicM[j][i] = cubic[n -(i+1)][j];
                System.out.print(cubicM[j][i]+" ");
            }
            System.out.println();
        }

    }
}```
-------

### Task : Cinema

- n,m배열인 영화관이 있다 배열의 요소가 0이면 자리가 있고 1이면 자리가 없다.
- 연속된 k자리가 비어있는지 확인하고 자리가 있으면 그 자리의 열을 출력하고 자리가 없으면 0 을 출력하라. 


- Pattern , Matcher를 사용하는 방법 
-  정규식을 사용해야만 풀리는 문제가 아니기 때문에 굳이 이렇게 까지 할 필요는 없는것 같다.

```
import java.util.Scanner;
import java.util.regex.Matcher;
import java.util.regex.Pattern;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int m = scanner.nextInt();
        int k = 0;
        int cinema[][] = new int[n][m];

        for (int i = 0; i < cinema.length; i++) {
            for (int j = 0; j < cinema[i].length; j++) {
                cinema[i][j] = scanner.nextInt();
            }
        }
        k = scanner.nextInt();
        String regex = String.format("[0]{%d}", k);
        Pattern p = Pattern.compile(regex);

        for (int i = 0; i < cinema.length; i++) {
            String row = "";
            for (int j = 0; j < cinema[i].length; j++) {
                row = row + cinema[i][j];
            }
            Matcher match = p.matcher(row);
            if (match.find()) {
                System.out.println(i + 1);
                break;
            } else if (i == cinema.length - 1) {
                System.out.println(0);
            }
        }
    }
}
```
- 연속된 0 이 들어가는 지 확인 할 때 counter를 리셋해주는 방법이 있다.

```
import java.util.Scanner;

class Main {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int counter = 0;
        int n = scanner.nextInt();
        int m = scanner.nextInt();
        int k =0;
        int cinema[][] = new int[n][m];

        for (int i = 0; i < cinema.length; i++) {
            for (int j = 0; j < cinema[0].length; j++) {
                cinema[i][j] = scanner.nextInt();
            }
        }
        k = scanner.nextInt();
        for (int i = 0; i < cinema.length; i++) {
            if (counter == k) {
                break;
            }
            counter = 0;
            for (int j = 0; j < cinema[0].length; j++) {
                if (cinema[i][j] == 0) {
                    counter++;
                    if (counter == k) {
                        System.out.println(i + 1);
                        break;
                    }
                } else {
                    counter = 0;
                }
            }
        }
        if (counter < k) {
            System.out.println(0);
        }
    }
```

-------

### Task :
- 
-

```

```
-------
