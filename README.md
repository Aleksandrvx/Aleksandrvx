import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        char userInput;

        while (true) {
            System.out.print("Wpisz literę 'T', 't', 'N' lub 'n': ");
            String input = scanner.nextLine();
            if (input.length() == 1) {
                userInput = input.charAt(0);
                if (userInput == 'T' || userInput == 't' || userInput == 'N' || userInput == 'n') {
                    System.out.println("Dziękuję! Podałeś poprawną literę.");
                    break;
                }
            }
            System.out.println("Niepoprawna litera. Spróbuj ponownie.");
        }

        scanner.close();
    }
}
