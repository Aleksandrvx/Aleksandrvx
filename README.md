import java.util.Random;
import java.util.Scanner;

public class Zad16 {

    public static int wyborKomputera() {
        Random random = new Random();
        return random.nextInt(3) + 1; // 1 - kamień, 2 - papier, 3 - nożyce
    }

    public static int wyborUzytkownika() {
        Scanner scanner = new Scanner(System.in);
        int wybor;

        do {
            System.out.println("Wybierz opcję:");
            System.out.println("1 - Kamień");
            System.out.println("2 - Papier");
            System.out.println("3 - Nożyce");
            System.out.print("Twój wybór: ");
            wybor = scanner.nextInt();

            if (wybor < 1 || wybor > 3) {
                System.out.println("Nieprawidłowy wybór! Wybierz 1, 2 lub 3.");
            }
        } while (wybor < 1 || wybor > 3);

        return wybor;
    }

    public static void pokazWybor(int wybor, String kto) {
        String nazwa = switch (wybor) {
            case 1 -> "Kamień";
            case 2 -> "Papier";
            case 3 -> "Nożyce";
            default -> "Nieznany";
        };
        System.out.println(kto + " wybrał: " + nazwa);
    }

    public static void okreslZwyciezce(int wyborUzytkownika, int wyborKomputera) {
        if (wyborUzytkownika == wyborKomputera) {
            System.out.println("Remis! Zagraj ponownie.");
        } else if ((wyborUzytkownika == 1 && wyborKomputera == 3) ||
                   (wyborUzytkownika == 2 && wyborKomputera == 1) ||
                   (wyborUzytkownika == 3 && wyborKomputera == 2)) {
            System.out.println("Gratulacje! Wygrałeś!");
        } else {
            System.out.println("Przegrałeś! Komputer wygrywa.");
        }
    }

    public static void main(String[] args) {
        int wyborKomputera = wyborKomputera();
        int wyborUzytkownika = wyborUzytkownika();

        pokazWybor(wyborUzytkownika, "Ty");
        pokazWybor(wyborKomputera, "Komputer");

        okreslZwyciezce(wyborUzytkownika, wyborKomputera);
    }
}
