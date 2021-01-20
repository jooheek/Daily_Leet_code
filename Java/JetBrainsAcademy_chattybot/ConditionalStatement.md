### Task : Chocolate

- N * M �� ���·� ������� ���ݸ��� �ִ�. �� ���ݸ��� ������ K �������� ����������� true �ƴϸ� false�� ����϶�

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt();
        int M = scanner.nextInt();
        int K = scanner.nextInt();
        int nMultiple[] = new int[M];
        int mMultiple[] = new int[N];
        boolean nContains = false;
        boolean mContains = false;
        
        //���� K�� N,M�� ����̸� TRUE
        //�ƴ� FALSE
        //N�� ��� 1.2.3....M
        //M�� ��� 1.2.3....N
        for(int i =0; i<M;i++){
            nMultiple[i] = N*(i+1);
        }
        for(int i =0; i<N;i++){
            mMultiple[i] = M*(i+1);
        }
        //�ܾʵ�?
//        if(Arrays.asList(nMultiple).contains(K)){
//            System.out.println(1);
//        }

        for(Integer s: nMultiple){
            if(s.equals(K)){
                nContains = true;
            }
        }

        for(Integer s: mMultiple){
            if(s.equals(K)){
                mContains = true;
            }
        }
        System.out.println(nContains || mContains);
    }
}

```
- ������ ���� �ߴ�... �ʹ� ���� ����� �־���.

```
K<= N * M && (K % N == 0 || K % M == 0)
```
