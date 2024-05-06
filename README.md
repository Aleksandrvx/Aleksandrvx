import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Inicjalizacja skanera do pobierania danych od użytkownika
        Scanner scanner = new Scanner(System.in);

        // Prośba o wprowadzenie wagi i wzrostu
        System.out.println("Podaj wagę w kilogramach: ");
        double waga = scanner.nextDouble();

        System.out.println("Podaj wzrost w metrach: ");
        double wzrost = scanner.nextDouble();

        // Obliczenie indeksu BMI
        double bmi = waga / (wzrost * wzrost);

        // Wyświetlenie indeksu BMI
        System.out.println("Twój indeks BMI wynosi: " + bmi);

        // Sprawdzenie zakresu indeksu BMI i wyświetlenie odpowiedniego komunikatu
        if (bmi < 18.5) {
            System.out.println("Niedowaga");
        } else if (bmi >= 18.5 && bmi <= 25) {
            System.out.println("Optymalna waga");
        } else {
            System.out.println("Nadwaga");
        }

        // Zamknięcie skanera
        scanner.close();
    }
}
