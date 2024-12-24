import java.util.Random;
import java.util.Scanner;

public class NumberGuessingGame {
    public static int playRound() {
        Random random = new Random();
        int numberToGuess = random.nextInt(100) + 1;
        int attempts = 0;
        int maxAttempts = 10;
        System.out.println("\nWelcome to the Number Guessing Game!");
        System.out.println(
                "I'm thinking of a number between 1 and 100. You have " + maxAttempts + " attempts to guess it.");
        Scanner scanner = new Scanner(System.in);
        while (attempts < maxAttempts) {
            System.out.print("Enter your guess: ");
            int guess = scanner.nextInt();
            attempts++;
            if (guess < numberToGuess) {
                System.out.println("Your guess is too low!");
            } else if (guess > numberToGuess) {
                System.out.println("Your guess is too high!");
            } else {
                System.out.println("Congratulations! You've guessed the number " + numberToGuess + " in " + attempts
                        + " attempts!");
                return attempts;
            }
        }

        System.out.println(
                "Sorry, you've used all " + maxAttempts + " attempts! The correct number was " + numberToGuess + ".");
        return maxAttempts;
    }

    public static void playGame() {
        int roundsPlayed = 0;
        int roundsWon = 0;
        int totalAttempts = 0;
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.println("\nNew Round!");
            roundsPlayed++;
            int attemptsTaken = playRound();
            totalAttempts += attemptsTaken;

            if (attemptsTaken < 10) {
                roundsWon++;
            }

            System.out.print("\nDo you want to play another round? (yes/no): ");
            String playAgain = scanner.next().toLowerCase();

            if (!playAgain.equals("yes")) {
                break;
            }
        }
        System.out.println("\nGame Over! You played " + roundsPlayed + " rounds and won " + roundsWon + " of them.");
        System.out.println("You took " + totalAttempts + " attempts in total.");
    }

    public static void main(String[] args) {
        playGame();
    }
}
