import java.util.Scanner;

public class KalkulatorCzasu {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Podaj liczbę sekund: ");
        int sekundy = scanner.nextInt();

        int dni = sekundy / 86400;
        sekundy %= 86400;
        int godziny = sekundy / 3600;
        sekundy %= 3600;
        int minuty = sekundy / 60;
        sekundy %= 60;

        System.out.println(sekundy + " sekund to " + dni + " dni, " + godziny + " godzin, " + minuty + " minut i " + sekundy + " sekund.");
    }
}
