###Task : find the roots of a cubic equation

- ax^3+bx^2+cx+d=0 �Լ��� �����ϴ� �ظ� ���϶� 
- 0���� 1000 ����

`import java.util.Scanner;

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
}`

__ __ __ __ __ __ __

##Grades
-�������� �𸣰����� 2���� 5������� ������ �ű��
- 5-> A, 4->B, 3->C, 2->D
-�л����� n��
<br/>

`import java.util.Scanner;

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
}`

