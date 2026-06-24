 Codsoft-Task-1
Number Game
https://onecompiler.com/java/44ss9zq28

import java.util.Random;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        Random rand = new Random();

        int num = rand.nextInt(100) + 1;
        int estimate = 0;
        int pursue = 0;

        System.out.println("Guess a number between 1 and 100");

        while (estimate != num) {

            System.out.print("Enter your estimate: ");
            estimate = sc.nextInt();
            pursue++;

            if (estimate > num) {
                System.out.println("high num");
            } else if (estimate < num) {
                System.out.println("low num");
            } else {
                System.out.println("Correct");
                System.out.println("Pursue taken: " + pursue);
            }
        }

        sc.close();
    }
}
