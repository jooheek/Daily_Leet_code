### Task : Chocolate

- N * M 의 형태로 만들어진 초콜릿이 있다. 이 초콜릿의 조각을 K 조각으로 떼어낼수있으면 true 아니면 false를 출력하라

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
        
        //만약 K가 N,M의 배수이면 TRUE
        //아님 FALSE
        //N의 배수 1.2.3....M
        //M의 배수 1.2.3....N
        for(int i =0; i<M;i++){
            nMultiple[i] = N*(i+1);
        }
        for(int i =0; i<N;i++){
            mMultiple[i] = M*(i+1);
        }
        //외않되?
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
- 삽질을 한참 했다... 너무 쉬운 방법이 있었음.

```
K<= N * M && (K % N == 0 || K % M == 0)
```
