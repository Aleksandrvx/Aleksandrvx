import java.util.Scanner;

public class Zad2 {
    public static double obliczCeneDetaliczna(double cenaHurtowa, double marzaProcentowa) {
        return cenaHurtowa + (cenaHurtowa * (marzaProcentowa / 100));
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj cenę hurtową produktu (w zł): ");
        double cenaHurtowa = scanner.nextDouble();

        System.out.print("Podaj marżę w procentach: ");
        double marzaProcentowa = scanner.nextDouble();

        double cenaDetaliczna = obliczCeneDetaliczna(cenaHurtowa, marzaProcentowa);

        System.out.printf("Cena detaliczna produktu wynosi: %.2f zł%n", cenaDetaliczna);

        scanner.close();
    }
}





import java.util.Scanner;

public class Zad3 {
    private static final double LITRY_NA_10M2 = 1.5;
    private static final double GODZINY_NA_10M2 = 8;
    private static final double KOSZT_GODZINY = 18.0;

    public static double obliczLiczbeLitrow(double powierzchnia) {
        return (powierzchnia / 10) * LITRY_NA_10M2;
    }

    public static double obliczLiczbeGodzin(double powierzchnia) {
        return (powierzchnia / 10) * GODZINY_NA_10M2;
    }

    public static double obliczKosztFarby(double liczbaLitrow, double cenaZaLitr) {
        return liczbaLitrow * cenaZaLitr;
    }

    public static double obliczKosztRobocizny(double liczbaGodzin) {
        return liczbaGodzin * KOSZT_GODZINY;
    }

    public static double obliczLacznyKoszt(double kosztFarby, double kosztRobocizny) {
        return kosztFarby + kosztRobocizny;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj liczbę pokojów do pomalowania: ");
        int liczbaPokojow = scanner.nextInt();

        System.out.print("Podaj cenę farby za litr (w zł): ");
        double cenaFarbyZaLitr = scanner.nextDouble();

        double calkowitaPowierzchnia = 0;

        for (int i = 1; i <= liczbaPokojow; i++) {
            System.out.print("Podaj powierzchnię pokoju nr " + i + " (w m²): ");
            calkowitaPowierzchnia += scanner.nextDouble();
        }

        double potrzebneLitry = obliczLiczbeLitrow(calkowitaPowierzchnia);
        double potrzebneGodziny = obliczLiczbeGodzin(calkowitaPowierzchnia);
        double kosztFarby = obliczKosztFarby(potrzebneLitry, cenaFarbyZaLitr);
        double kosztRobocizny = obliczKosztRobocizny(potrzebneGodziny);
        double lacznyKoszt = obliczLacznyKoszt(kosztFarby, kosztRobocizny);


        System.out.println("\n=== Podsumowanie kosztów malowania ===");
        System.out.printf("Łączna powierzchnia: %.2f m²%n", calkowitaPowierzchnia);
        System.out.printf("Potrzebna ilość farby: %.2f litrów%n", potrzebneLitry);
        System.out.printf("Potrzebny czas pracy: %.2f godzin%n", potrzebneGodziny);
        System.out.printf("Koszt farby: %.2f zł%n", kosztFarby);
        System.out.printf("Koszt robocizny: %.2f zł%n", kosztRobocizny);
        System.out.printf("Łączny koszt malowania: %.2f zł%n", lacznyKoszt);

        scanner.close();
    }
}
