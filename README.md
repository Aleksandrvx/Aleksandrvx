import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Inicjalizacja skanera do pobierania danych od użytkownika
        Scanner scanner = new Scanner(System.in);

        // Prośba o wprowadzenie trzech wyników testów
        System.out.println("Podaj wynik testu 1: ");
        int wynikTestu1 = scanner.nextInt();

        System.out.println("Podaj wynik testu 2: ");
        int wynikTestu2 = scanner.nextInt();

        System.out.println("Podaj wynik testu 3: ");
        int wynikTestu3 = scanner.nextInt();

        // Obliczenie średniej wyników testów
        double srednia = (wynikTestu1 + wynikTestu2 + wynikTestu3) / 3.0;

        // Określenie oceny na podstawie średniej wyników testów
        char ocena;
        if (srednia >= 90) {
            ocena = '5';
        } else if (srednia >= 80) {
            ocena = '4';
        } else if (srednia >= 70) {
            ocena = '3';
        } else if (srednia >= 60) {
            ocena = '2';
        } else {
            ocena = '1';
        }

        // Wyświetlenie średniej wyników testów i oceny
        System.out.println("Średnia wyników testów: " + srednia);
        System.out.println("Ocena: " + ocena);

        // Zamknięcie skanera
        scanner.close();
    }
}
