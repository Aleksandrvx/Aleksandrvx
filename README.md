public class Zad13 {

    public static boolean czyPierwsza(int liczba) {
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
        for (int liczba = 1; liczba <= 10000; liczba++) {
            if (czyPierwsza(liczba)) {
                System.out.println(liczba);
            }
        }
    }
}





import java.util.Random;

public class Zad14 {

    public static boolean isEven(int liczba) {
        return liczba % 2 == 0;
    }

    public static void main(String[] args) {
        Random random = new Random();
        int parzyste = 0;
        int nieparzyste = 0;

        for (int i = 0; i < 100; i++) {
            int liczba = random.nextInt(1000); // Losowa liczba od 0 do 999

            if (isEven(liczba)) {
                parzyste++;
            } else {
                nieparzyste++;
            }
        }

        System.out.println("Liczba parzystych: " + parzyste);
        System.out.println("Liczba nieparzystych: " + nieparzyste);
    }
}
