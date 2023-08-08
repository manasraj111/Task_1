# Task_1 Number guessing game (Using Java)


import java.util.Scanner;
 
public class Question_1 {
    public static void
    guessingNumberGame()
    {
        Scanner sc = new Scanner(System.in);
        int number = 1 + (int)(100
                               * Math.random());
        int K = 5;
 
        int i, guess;
 
        System.out.println("The number between 1 to 100 is to be chosen within 5 chances:");
 
        
        for (i = 0; i < K; i++) {
 
            System.out.println(
                "Guess the number:");
 
            
            guess = sc.nextInt();
 
            
            if (number == guess) {
                System.out.println("CONGRATULATIONS !!.....You are passed");
                break;
            }
            else if (number > guess
                     && i != K - 1) {
                System.out.println("The number is greater than : " + guess);
            }
            else if (number < guess
                     && i != K - 1) {
                System.out.println("The number is less than : " + guess);
            }
        }
 
        if (i == K) {
            System.out.println("You are exhausted");
 
            System.out.println(
                "The number was : " + number);
        }
    }
 
    
    public static void
    main(String arg[])
    {
 
        guessingNumberGame();
    }
}
