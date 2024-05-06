import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Inicjalizacja tablicy z liczbami rzymskimi
        String[] rzymskie = {"I", "II", "III", "IV", "V", "VI", "VII", "VIII", "IX", "X"};

        // Inicjalizacja skanera do pobierania danych od użytkownika
        Scanner scanner = new Scanner(System.in);

        // Prośba o wprowadzenie wartości z przedziału od 1 do 10
        System.out.println("Podaj liczbę z przedziału od 1 do 10: ");
        int liczba = scanner.nextInt();

        // Sprawdzenie, czy liczba należy do przedziału od 1 do 10
        if (liczba < 1 || liczba > 10) {
            System.out.println("Błąd: Podana liczba nie należy do przedziału od 1 do 10.");
        } else {
            // Wyświetlenie liczby rzymskiej odpowiadającej podanej wartości
            System.out.println("Liczba rzymska: " + rzymskie[liczba - 1]);
        }

        // Zamknięcie skanera
        scanner.close();
    }
}
