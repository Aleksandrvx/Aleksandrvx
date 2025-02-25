import java.util.Scanner;

public class Zad11 {

    public static double kineticEnergy(double masa, double predkosc) {
        return 0.5 * masa * predkosc * predkosc;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj masę obiektu w kilogramach: ");
        double masa = scanner.nextDouble();

        System.out.print("Podaj prędkość obiektu w metrach na sekundę: ");
        double predkosc = scanner.nextDouble();

        double energia = kineticEnergy(masa, predkosc);

        System.out.println("Energia kinetyczna obiektu wynosi: " + energia + " J");

        scanner.close();
    }
}






import java.util.Scanner;

public class Zad12 {

    public static boolean isPrime(int liczba) {
        if (liczba <= 1) {
            return false;
        }
        for (int i = 2; i <= Math.sqrt(liczba); i++) {
            if (liczba % i == 0) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj liczbę do sprawdzenia, czy jest pierwsza: ");
        int liczba = scanner.nextInt();

        if (isPrime(liczba)) {
            System.out.println(liczba + " jest liczbą pierwszą.");
        } else {
            System.out.println(liczba + " nie jest liczbą pierwszą.");
        }

        scanner.close();
    }
}
