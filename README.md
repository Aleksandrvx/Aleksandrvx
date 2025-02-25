public class Zad4 {
    private static final double G = 9.8;

    public static double fallingDistance(int czas) {
        return 0.5 * G * czas * czas;
    }

    public static void main(String[] args) {
        System.out.println("Czas (s) | Odległość (m)");
        System.out.println("------------------------");
        for (int t = 1; t <= 10; t++) {
            System.out.printf("%8d | %12.2f%n", t, fallingDistance(t));
        }
    }
}



public class Zad5 {
    public static double celsius(int fahrenheit) {
        return (5.0 / 9.0) * (fahrenheit - 32);
    }

    public static void main(String[] args) {

        System.out.println("Fahrenheit | Celsius");
        System.out.println("---------------------");

        for (int f = 0; f <= 20; f++) {
            System.out.printf("%10d | %7.2f%n", f, celsius(f));
        }
    }
}




import java.util.Scanner;

public class Zad6 {
    public static double calcAverage(int t1, int t2, int t3, int t4, int t5) {
        return (t1 + t2 + t3 + t4 + t5) / 5.0;
    }

    public static int determineGrade(int wynik) {
        if (wynik >= 90) return 5;
        else if (wynik >= 80) return 4;
        else if (wynik >= 70) return 3;
        else if (wynik >= 60) return 2;
        else return 1;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] wyniki = new int[5];

        for (int i = 0; i < 5; i++) {
            System.out.print("Podaj wynik testu " + (i + 1) + ": ");
            wyniki[i] = scanner.nextInt();
        }

        System.out.println("\nWyniki testów i ich oceny:");
        for (int i = 0; i < 5; i++) {
            System.out.println("Test " + (i + 1) + ": " + wyniki[i] + " - Ocena: " + determineGrade(wyniki[i]));
        }

        double srednia = calcAverage(wyniki[0], wyniki[1], wyniki[2], wyniki[3], wyniki[4]);
        System.out.printf("\nŚrednia z testów: %.2f\n", srednia);
        System.out.println("Ocena końcowa: " + determineGrade((int) srednia));

        scanner.close();
    }
}
