import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String userInput;

        while (true) {
            System.out.print("Wpisz tekst 'Tak' lub 'Nie': ");
            userInput = scanner.nextLine();
            if (userInput.equalsIgnoreCase("Tak") || userInput.equalsIgnoreCase("Nie")) {
                System.out.println("Dziękuję! Podałeś poprawny tekst.");
                break;
            } else {
                System.out.println("Niepoprawny tekst. Spróbuj ponownie.");
            }
        }

        scanner.close();
    }
}
