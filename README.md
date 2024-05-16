import java.util.Scanner;

public class ObliczCiezar {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Podaj masę obiektu w kilogramach: ");
        double masa = scanner.nextDouble();
        double ciezar = obliczCiezar(masa);

        if (ciezar > 1000) {
            System.out.println("Obiekt jest zbyt ciężki.");
        } else if (ciezar < 10) {
            System.out.println("Obiekt jest za lekki.");
        } else {
            System.out.println("Ciężar obiektu wynosi: " + ciezar + " niutonów.");
        }
    }

    public static double obliczCiezar(double masa) {
        return masa * 9.8;
    }
}
