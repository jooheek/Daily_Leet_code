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
- 메소드 기능별로 묶어서 수정함 

```
package machine;

import java.util.Scanner;

public class CoffeeMachine {
    private static int water = 400;
    private static int milk = 540;
    private static int coffeeBean = 120;
    private static int cups = 9;
    private static int money = 550;

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        printStock();
        printAction();
        String choice = scanner.next();

        if(choice.equals("buy") ){
            System.out.print("What do you want to buy? 1 - espresso, 2 - latte, 3 - cappuccino: \n" +
                    "> ");
            int beverage = scanner.nextInt();
            switch (beverage){
                case 1:
                    water -= 250;
                    coffeeBean -= 16;
                    cups -= 1;
                    money += 4;
                    break;
                case 2:
                    water -= 350;
                    milk -= 75;
                    coffeeBean -= 20;
                    cups -= 1;
                    money += 7;
                    break;
                case 3:
                    water -= 200;
                    milk -= 100;
                    coffeeBean -= 12;
                    cups -= 1;
                    money += 6;
                    break;
                default :
                    System.out.println("choose one");
                    break;
            }
            printStock();
        }else if(choice.equals("fill") ){
            System.out.print("Write how many ml of water do you want to add: \n" +
                    ">");
            water += scanner.nextInt();
            System.out.print("Write how many ml of milk do you want to add: \n" +
                    ">");
            milk += scanner.nextInt();
            System.out.print("Write how many grams of coffee beans do you want to add: \n" +
                    "> ");
            coffeeBean += scanner.nextInt();
            System.out.print("Write how many disposable cups of coffee do you want to add: \n" +
                    "> ");
            cups += scanner.nextInt();

            printStock();
        }else if(choice.equals("take") ){
            System.out.println("I gave you $"+money);
            money = 0;
            printStock();
        }
    }

    public static void printStock(){
       System.out.println("\nThe coffee machine has:\n" +
                water+" of water\n" +
                milk+" of milk\n" +
                coffeeBean+" of coffee beans\n" +
                cups+" of disposable cups\n" +
                "$"+money+" of money\n");
    }

    public static void printAction(){
        System.out.print("Write action (buy, fill, take, remaining, exit): \n" +
                "> ");

    }


}
```



---



Task : Coffee Machine 2

- 커피머신에 400ml물, 540ml 우유, 120g 커피빈, 9개의 컵이 있다. 
- 에스프레소, 라떼, 카푸치노를 살수있고(buy) 커피머신에 내용물을 충전할 수 있고(fill) 커피머신에 있는 돈을 뽑을수있다.(take)
```
import java.util.Scanner;

public class CoffeeMachine {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int water = 400;
        int milk = 540;
        int coffeeBean = 120;
        int cups = 9;
        int money = 550;

        System.out.println("The coffee machine has:\n" +
                water+" of water\n" +
                milk+" of milk\n" +
                coffeeBean+" of coffee beans\n" +
                cups+" of disposable cups\n" +
                money+" of money\n");

        System.out.print("Write action (buy, fill, take): \n" +
                ">");

        String choice = scanner.next();

        if(choice.equals("buy") ){
            System.out.print("What do you want to buy? 1 - espresso, 2 - latte, 3 - cappuccino: \n" +
                    "> ");
            int beverage = scanner.nextInt();
            switch (beverage){
                case 1:
                    water = water - 250;
                    coffeeBean = coffeeBean -16;
                    cups = cups -1;
                    money = money + 4;
                    break;
                case 2:
                    water = water -350;
                    milk = milk -75;
                    coffeeBean = coffeeBean - 20;
                    cups = cups -1;
                    money = money +7;
                    break;
                case 3:
                    water = water -200;
                    milk = milk-100;
                    coffeeBean = coffeeBean -12;
                    cups = cups -1;
                    money = money +6;
                    break;
                default :
                    System.out.println("choose one");
                    break;
            }
        }else if(choice.equals("fill") ){
            System.out.print("Write how many ml of water do you want to add: \n" +
                    ">");
            int addWater = scanner.nextInt();
            System.out.print("Write how many ml of milk do you want to add: \n" +
                    ">");
            int addMilk = scanner.nextInt();
            System.out.print("Write how many grams of coffee beans do you want to add: \n" +
                    "> ");
            int addCoffeeBean = scanner.nextInt();
            System.out.print("Write how many disposable cups of coffee do you want to add: \n" +
                    "> ");
            int addCup = scanner.nextInt();

            water = water +addWater;
            milk = milk + addMilk;
            coffeeBean = coffeeBean + addCoffeeBean;
            cups = cups + addCup;

        }else if(choice.equals("take") ){
            System.out.println("I gave you $550");
            money = 0;
        }else{
            System.out.println("nope!");
        }

        System.out.println("\nThe coffee machine has:\n" +
                water+" of water\n" +
                milk+" of milk\n" +
                coffeeBean+" of coffee beans\n" +
                cups+" of disposable cups\n" +
                money+" of money");

    }
}
```