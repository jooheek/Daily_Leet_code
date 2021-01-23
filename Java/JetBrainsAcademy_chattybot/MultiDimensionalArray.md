### Task : Fill the matrix by numbers
- n�� �Է¹����� n x n�� ���·� �簢���� �׷����� 
![picture of Array](https://postfiles.pstatic.net/MjAyMTAxMjBfMTA2/MDAxNjExMTM2NTgyNjM0.yU8qdB-HK1ZfgmiCv7qpi5b5dD8GjHJDorooD4_Jzvsg.YW1UzLBE7aHe0rfca4gN0dUpAItf2h3C-4IOyvfaFggg.PNG.kimjoohee713/%EB%B0%B0%EC%97%B4.png?type=w966)
- ���� ���°� �ȴ�. �迭�� ����϶�.

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
- �迭�� �� ����Ѵٴ� ������ ������.

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
- n X m �迭�� �Էµȴ� �� �迭�� �ð�������� 90�� ���� �迭�� ����϶�.
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

### Task :
- 
-

```
```
-------

### Task :
- 
-

```
```
-------
