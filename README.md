import java.util.Scanner;

public class Zad9 {

    public static double obliczZysk(int liczbaAkcji, double cenaZakupu, double prowizjaZakup,
                                    double cenaSprzedazy, double prowizjaSprzedaz) {
        return ((liczbaAkcji * cenaSprzedazy) - prowizjaSprzedaz) - 
               ((liczbaAkcji * cenaZakupu) + prowizjaZakup);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj liczbę akcji: ");
        int liczbaAkcji = scanner.nextInt();

        System.out.print("Podaj cenę zakupu jednej akcji: ");
        double cenaZakupu = scanner.nextDouble();

        System.out.print("Podaj prowizję od zakupu: ");
        double prowizjaZakup = scanner.nextDouble();

        System.out.print("Podaj cenę sprzedaży jednej akcji: ");
        double cenaSprzedazy = scanner.nextDouble();

        System.out.print("Podaj prowizję od sprzedaży: ");
        double prowizjaSprzedaz = scanner.nextDouble();

        double zysk = obliczZysk(liczbaAkcji, cenaZakupu, prowizjaZakup, cenaSprzedazy, prowizjaSprzedaz);

        if (zysk > 0) {
            System.out.println("Zysk wynosi: " + zysk + " zł.");
        } else if (zysk < 0) {
            System.out.println("Strata wynosi: " + (-zysk) + " zł.");
        } else {
            System.out.println("Nie ma ani zysku, ani straty.");
        }

        scanner.close();
    }
}




import java.util.Scanner;

public class Zad10 {

    public static double obliczZysk(int liczbaAkcji, double cenaZakupu, double prowizjaZakup,
                                    double cenaSprzedazy, double prowizjaSprzedaz) {
        return ((liczbaAkcji * cenaSprzedazy) - prowizjaSprzedaz) - 
               ((liczbaAkcji * cenaZakupu) + prowizjaZakup);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double sumaZyskow = 0;  // Przechowuje łączny zysk/stratę
        int liczbaFirm;  

        System.out.print("Podaj liczbę firm, dla których chcesz obliczyć zysk/stratę: ");
        liczbaFirm = scanner.nextInt();

        for (int i = 1; i <= liczbaFirm; i++) {
            System.out.println("\nFirma " + i + ":");

            System.out.print("Podaj liczbę akcji: ");
            int liczbaAkcji = scanner.nextInt();

            System.out.print("Podaj cenę zakupu jednej akcji: ");
            double cenaZakupu = scanner.nextDouble();

            System.out.print("Podaj prowizję od zakupu: ");
            double prowizjaZakup = scanner.nextDouble();

            System.out.print("Podaj cenę sprzedaży jednej akcji: ");
            double cenaSprzedazy = scanner.nextDouble();

            System.out.print("Podaj prowizję od sprzedaży: ");
            double prowizjaSprzedaz = scanner.nextDouble();

            double zysk = obliczZysk(liczbaAkcji, cenaZakupu, prowizjaZakup, cenaSprzedazy, prowizjaSprzedaz);
            sumaZyskow += zysk; // Sumowanie wyniku

            if (zysk > 0) {
                System.out.println("Zysk dla tej firmy: " + zysk + " zł.");
            } else if (zysk < 0) {
                System.out.println("Strata dla tej firmy: " + (-zysk) + " zł.");
            } else {
                System.out.println("Brak zysku i straty dla tej firmy.");
            }
        }

        System.out.println("\nŁączny wynik ze sprzedaży akcji:");
        if (sumaZyskow > 0) {
            System.out.println("Łączny zysk: " + sumaZyskow + " zł.");
        } else if (sumaZyskow < 0) {
            System.out.println("Łączna strata: " + (-sumaZyskow) + " zł.");
        } else {
            System.out.println("Nie ma ani zysku, ani straty.");
        }

        scanner.close();
    }
}
