// Secret-word-checker
import java.util.Scanner;

class SecretWord {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String[] words = {"java", "array", "loop", "string", "computer"};

        System.out.print("Guess the secret word: ");
        String guess = sc.nextLine();

        boolean found = false;

        for (String word : words) {
            if (word.equalsIgnoreCase(guess)) {
                found = true;
                break;
            }
        }

        if (found)
            System.out.println("Correct! You found a secret word!");
        else
            System.out.println("Wrong! Try again.");

        sc.close();
    }
}
