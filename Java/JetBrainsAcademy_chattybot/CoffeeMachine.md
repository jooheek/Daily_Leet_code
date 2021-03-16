Task : 커피머신 만들기

- 커피 한 잔을 만드는데 200ml 물, 50ml 우유, 15g의 커피빈이 필요하다.
- 요청된 커피를 추출할수있다면 "Yes, I can make that amount of coffee" 라고 출력되고 요청된 커피보다 더 추출할수 있다면 "(and even N more than that)"를 붙인다.
- 요청된 커피를 추출할 수 없다면 "No, I can make only N cup(s) of coffee"라고 출력한다.

```
import java.util.Scanner;

public class CoffeeMachine {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Write how many ml of water the coffee machine has: \n" +
                "> ");
        int water = scanner.nextInt();
        System.out.print("Write how many ml of milk the coffee machine has: \n" +
                "> ");
        int milk = scanner.nextInt();
        System.out.print("Write how many grams of coffee beans the coffee machine has: \n" +
                "> ");
        int coffeeBean = scanner.nextInt();
        System.out.print("Write how many cups of coffee you will need: \n" +
                "> ");
        int cupOfCoffee = scanner.nextInt();

        String success= "Yes, I can make that amount of coffee";

        // 200, 50, 15로 나눠서 몫을 구함 
        // 그 수중 가장 작은 수 == 기계가 만들수 있는 커피의 갯수
        int quotientWater = water/200;
        int quotientMilk = milk/50;
        int quotientCoffeeBean = coffeeBean/15;

        //최소값을 구할 int 배열
        int array[] = {quotientWater,quotientMilk,quotientCoffeeBean};

        int min = array[0]; //최소값
        for(int i=0;i<array.length;i++) {
            if (min > array[i]) {
                //min의 값보다 array[i]이 작으면 min = array[i]
                min = array[i];
            }
        }

      //  System.out.println("최소값 : "+min);
        
        if(quotientCoffeeBean >= cupOfCoffee && quotientMilk >= cupOfCoffee && quotientWater >= cupOfCoffee){
            //accurate
            System.out.println(min == cupOfCoffee ? success : success+" (and even "+(min-cupOfCoffee)+" more than that)");
        }else  {
            System.out.println("No, I can make only "+min+" cup(s) of coffee");
        }

    }
}
```