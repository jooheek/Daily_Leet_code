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
### Task :
- 
-

```
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
        //3 4
        //11 12 13 14
        //21 22 23 24
        //31 32 33 34

        for(int i =0;i<m;i++){
            cubicM[0][i] = cubic[i][0];
        }
        //31 21 11
        //32 22 12
        //33 23 13
        //34 24 14
        System.out.println(cubicM[0][0]+" "+cubicM[0][1]+" "+cubicM[0][2]+" ");
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
