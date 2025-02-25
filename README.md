import java.util.Scanner;

public class ShowCharacter {
    public static void showChar(String text, int index) {
        if (text == null || index < 0 || index >= text.length()) {
            System.out.println("Nieprawidłowa pozycja znaku.");
        } else {
            System.out.println("Znak na pozycji " + index + " to: " + text.charAt(index));
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj tekst: ");
        String cityName = scanner.nextLine();

        System.out.print("Podaj indeks znaku: ");
        int index = scanner.nextInt();

        showChar(cityName, index);

        scanner.close();
    }
}
