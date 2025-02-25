import java.util.Scanner;

public class Zad7 {
    public static void menu() {
        System.out.println("\n1. Przelicz na kilometry.");
        System.out.println("2. Przelicz na cale.");
        System.out.println("3. Przelicz na stopy.");
        System.out.println("4. Zamknij program.");
        System.out.print("Podaj wybraną opcję: ");
    }

    public static void showKilometers(double metry) {
        System.out.printf("%.2f metrów w kilometrach to %.3f km.\n", metry, metry * 0.001);
    }

    public static void showInches(double metry) {
        System.out.printf("%.2f metrów w calach to %.2f cali.\n", metry, metry * 39.37);
    }

    public static void showFeet(double metry) {
        System.out.printf("%.2f metrów w stopach to %.2f ft.\n", metry, metry * 3.281);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double metry;
        
        do {
            System.out.print("Podaj odległość w metrach (wartość nieujemna): ");
            metry = scanner.nextDouble();
            if (metry < 0) {
                System.out.println("Błąd! Odległość nie może być ujemna.");
            }
        } while (metry < 0);

        int opcja;
        do {
            menu();
            opcja = scanner.nextInt();
            
            switch (opcja) {
                case 1:
                    showKilometers(metry);
                    break;
                case 2:
                    showInches(metry);
                    break;
                case 3:
                    showFeet(metry);
                    break;
                case 4:
                    System.out.println("Żegnaj!");
                    break;
                default:
                    System.out.println("Błąd! Wybierz opcję 1-4.");
            }
        } while (opcja != 4);

        scanner.close();
    }
}


import java.util.Scanner;

public class Zad8 {

    public static double distance(double szybkosc, double czas) {
        return szybkosc * czas;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj szybkość pojazdu (w km/h): ");
        double szybkosc = scanner.nextDouble();

        System.out.print("Podaj czas podróży (w godzinach): ");
        double czas = scanner.nextDouble();

        double odleglosc = distance(szybkosc, czas);

        System.out.println("Przejechana odległość to: " + odleglosc + " km.");

        scanner.close();
    }
}
