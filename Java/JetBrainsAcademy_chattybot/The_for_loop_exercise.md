//Task : find the roots of a cubic equation

- ax^3+bx^2+cx+d=0 함수를 만족하는 해를 구하라
- 0에서 1000 사이

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


//Grades
- 5-> A, 4->B, 3->C, 2->D
- 