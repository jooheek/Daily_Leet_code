Task : Cinema

- 영화관 좌석을 보여주고 구매하고 메뉴에서 나가는 기능을 구현하라.

```
package cinema;

import java.util.Scanner;

public class Cinema {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("\n");
        System.out.println("Enter the number of rows:");
        int rows = scanner.nextInt();
        System.out.println("Enter the number of seats in each row:");
        int seatsInRow = scanner.nextInt();
        String [][] cinema = new String[rows + 1][seatsInRow + 1];
        cinema = createCinema(cinema);

        while (true) {
            printMenu();
            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    printSeats(cinema);
                    break;
                case 2:
                    System.out.println("\n");
                    System.out.println("Enter a row number:");
                    int myRow = scanner.nextInt();
                    System.out.println("Enter a seat number in that row:");
                    int mySeat = scanner.nextInt();
                    calculatePrice(myRow, rows, seatsInRow);
                    System.out.println();
                    mySeatInCinema(cinema, myRow, mySeat);
                    break;
                case 0:
                    return;
                default:
                    break;
            }
        }

    }

    static String[][] createCinema(String[][] cinema) {
        for (int i = 0; i < cinema.length; i++) {
            for (int j = 0; j < cinema[i].length; j++) {
                if (i == 0 && j == 0) {
                    cinema[i][j] = " ";
                } else if (i == 0 && j > 0) {
                    cinema[i][j] = " " + j;
                } else if (i > 0 && j == 0) {
                    cinema[i][j] = "\n" + i;
                } else {
                    cinema[i][j] = " S";
                }
            }
        }
        return cinema;
    }

    static void printMenu() {
        System.out.println();
        System.out.println("1. Show the seats");
        System.out.println("2. Buy a ticket");
        System.out.println("0. Exit");
    }

    static void printSeats(String[][] cinema) {
        System.out.println();
        System.out.println("Cinema:");
        for (int i = 0; i < cinema.length; i++) {
            for (int j = 0; j < cinema[i].length; j++) {
                if (j <= cinema[i].length) {
                    System.out.print(cinema[i][j]);
                } else {
                    System.out.println();
                }
            }
        }
        System.out.println();
    }

    static void calculatePrice(int myRow, int rows, int seatsInRow) {
        System.out.println();
        int seats = rows * seatsInRow;
        if (seats < 60) {
            System.out.println("Ticket price: $10");
        } else if (myRow <= rows / 2) {
            System.out.println("Ticket price: $10");
        } else {
            System.out.println("Ticket price: $8");
        }
    }

    static String[][] mySeatInCinema(String[][] cinema, int myRow, int mySeat) {
        cinema[myRow][mySeat] = " B";
        return cinema;
    }
}
``` 

- 영화관 배열을 만들고
- while 문 조건이 true면 무한반복으로 돌아간다.
-  0을 선택할 경우 return 으로 반복문을 끝낸다.


---
