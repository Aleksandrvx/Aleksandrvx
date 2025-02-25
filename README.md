import java.util.Random;
import java.util.Scanner;

public class GraKamienPapierNozyce {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        System.out.println("Witaj w grze 'Kamień, Papier, Nożyce'!");

        int graczWybor;

        while (true) {
            System.out.println("\nWybierz: ");
            System.out.println("1. Kamień");
            System.out.println("2. Papier");
            System.out.println("3. Nożyce");
            System.out.println("4. Wyjście");

            System.out.print("Podaj swój wybór (1-3) lub 4 aby zakończyć: ");
            graczWybor = scanner.nextInt();

            if (graczWybor == 4) {
                System.out.println("Dziękujemy za grę!");
                break;
            }

            if (graczWybor < 1 || graczWybor > 3) {
                System.out.println("Niepoprawny wybór! Wybierz liczbę od 1 do 3.");
                continue;
            }

            // Komputer losuje wybór
            int komputerWybor = random.nextInt(3) + 1; // Losuje liczbę 1, 2 lub 3

            String graczWybory = "";
            String komputerWybory = "";

            switch (graczWybor) {
                case 1:
                    graczWybory = "Kamień";
                    break;
                case 2:
                    graczWybory = "Papier";
                    break;
                case 3:
                    graczWybory = "Nożyce";
                    break;
            }

            switch (komputerWybor) {
                case 1:
                    komputerWybory = "Kamień";
                    break;
                case 2:
                    komputerWybory = "Papier";
                    break;
                case 3:
                    komputerWybory = "Nożyce";
                    break;
            }

            System.out.println("Komputer wybrał: " + komputerWybory);

            if (graczWybor == komputerWybor) {
                System.out.println("Remis! Obaj wybraliście " + graczWybory);
            } else if ((graczWybor == 1 && komputerWybor == 3) || (graczWybor == 2 && komputerWybor == 1) || (graczWybor == 3 && komputerWybor == 2)) {
                System.out.println("Wygrałeś! " + graczWybory + " wygrywa
