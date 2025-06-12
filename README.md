What Is a Number Guessing Game?
A Number Guessing Game is a simple interactive program where:

The computer randomly selects a number within a specified range (e.g., 1 to 100).

The user attempts to guess the number.

After each guess, the program provides feedback:

"Too low" if the guess is smaller than the target.

"Too high" if the guess is larger.

"Correct!" if the guess matches the target.

The game continues until the user guesses correctly or exhausts a predefined number of attempts.

🧰 Requirements
To implement this game in Java, you'll need:

Java Development Kit (JDK): Ensure you have the JDK installed on your system.

Integrated Development Environment (IDE): Use an IDE like IntelliJ IDEA, Eclipse, or NetBeans for writing and running your Java code.

Basic Java Knowledge: Familiarity with concepts like loops, conditionals, user input handling, and random number generation.

🧪 Step-by-Step Explanation
1. Import Necessary Classes
java
Copy
Edit
import java.util.Scanner;
import java.util.Random;
Scanner is used to capture user input.

Random generates random numbers.

2. Initialize Game Components
java
Copy
Edit
Scanner scanner = new Scanner(System.in);
Random random = new Random();
int numberToGuess = random.nextInt(100) + 1;
int userGuess = 0;
int attempts = 0;
numberToGuess holds the randomly generated number between 1 and 100.

userGuess stores the user's current guess.

attempts tracks the number of guesses made.

3. Display Welcome Message
java
Copy
Edit
System.out.println("Welcome to Number Guessing Game!");
System.out.println("Guess a number between 1 and 100:");
This introduces the game to the user.

4. Game Loop
java
Copy
Edit
while (userGuess != numberToGuess) {
    System.out.print("Enter your guess: ");
    userGuess = scanner.nextInt();
    attempts++;

    if (userGuess < numberToGuess) {
        System.out.println("Too low, try again!");
    } else if (userGuess > numberToGuess) {
        System.out.println("Too high, try again!");
    } else {
        System.out.println("Congratulations! You guessed the number in " + attempts + " attempts.");
    }
}
The loop continues until the user guesses correctly.

After each guess, feedback is provided to guide the user.

5. Close Scanner
java
Copy
Edit
scanner.close();
It's a good practice to close resources like Scanner to prevent memory leaks.

📊 Flowchart
To visualize the game's logic, here's a flowchart:


This diagram illustrates the game's flow from start to finish.

