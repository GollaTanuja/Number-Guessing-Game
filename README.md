# Number-Guessing-Game
The Number Guessing Game is a simple interactive game where the player tries to guess a randomly generated number within a specified range
import java.util.Scanner;

public class EasyNumberGuessing {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int numberToGuess = 50; // You can change this or use random logic
        int guess;
        int attempts = 0;
        int maxAttempts = 5;

        System.out.println("Welcome to the Number Guessing Game!");
        System.out.println("Guess the number between 1 and 100. You have " + maxAttempts + " attempts.");

        while (attempts < maxAttempts) {
            System.out.print("Enter your guess: ");
            guess = scanner.nextInt(); // Takes user input

            attempts++;

            if (guess == numberToGuess) {
                System.out.println("Congratulations! You guessed it right ");
                break;
            } else if (guess < numberToGuess) {
                System.out.println("Too low ");
            } else {
                System.out.println("Too high ");
            }

            System.out.println("Attempts left: " + (maxAttempts - attempts));
        }

        if (attempts == maxAttempts) {
            System.out.println("Sorry! You've used all attempts.");
            System.out.println("The correct number was: " + numberToGuess);
        }

        scanner.close();
    }
}

