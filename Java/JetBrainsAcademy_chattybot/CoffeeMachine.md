Task : Ŀ�Ǹӽ� �����

- Ŀ�� �� ���� ����µ� 200ml ��, 50ml ����, 15g�� Ŀ�Ǻ��� �ʿ��ϴ�.
- ��û�� Ŀ�Ǹ� �����Ҽ��ִٸ� "Yes, I can make that amount of coffee" ��� ��µǰ� ��û�� Ŀ�Ǻ��� �� �����Ҽ� �ִٸ� "(and even N more than that)"�� ���δ�.
- ��û�� Ŀ�Ǹ� ������ �� ���ٸ� "No, I can make only N cup(s) of coffee"��� ����Ѵ�.

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

        // 200, 50, 15�� ������ ���� ���� 
        // �� ���� ���� ���� �� == ��谡 ����� �ִ� Ŀ���� ����
        int quotientWater = water/200;
        int quotientMilk = milk/50;
        int quotientCoffeeBean = coffeeBean/15;

        //�ּҰ��� ���� int �迭
        int array[] = {quotientWater,quotientMilk,quotientCoffeeBean};

        int min = array[0]; //�ּҰ�
        for(int i=0;i<array.length;i++) {
            if (min > array[i]) {
                //min�� ������ array[i]�� ������ min = array[i]
                min = array[i];
            }
        }

      //  System.out.println("�ּҰ� : "+min);
        
        if(quotientCoffeeBean >= cupOfCoffee && quotientMilk >= cupOfCoffee && quotientWater >= cupOfCoffee){
            //accurate
            System.out.println(min == cupOfCoffee ? success : success+" (and even "+(min-cupOfCoffee)+" more than that)");
        }else  {
            System.out.println("No, I can make only "+min+" cup(s) of coffee");
        }

    }
}
```