import java.util.Scanner;

public class Zad15 {

    public static double presentValue(double przyszlaWartosc, double stopaOprocentowania, int liczbaLat) {
        return przyszlaWartosc / Math.pow(1 + stopaOprocentowania, liczbaLat);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj przyszłą wartość (np. 10000): ");
        double przyszlaWartosc = scanner.nextDouble();

        System.out.print("Podaj roczną stopę oprocentowania (np. 0.05 dla 5%): ");
        double stopaOprocentowania = scanner.nextDouble();

        System.out.print("Podaj liczbę lat: ");
        int liczbaLat = scanner.nextInt();

        double wartoscBiezaca = presentValue(przyszlaWartosc, stopaOprocentowania, liczbaLat);

        System.out.printf("Aby uzyskać %.2f zł po %d latach przy oprocentowaniu %.2f%%, musisz wpłacić teraz %.2f zł.\n",
                przyszlaWartosc, liczbaLat, stopaOprocentowania * 100, wartoscBiezaca);

        scanner.close();
    }
}
