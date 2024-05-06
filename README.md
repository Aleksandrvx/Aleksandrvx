
public class Main {
    public static void main(String[] args) {
        for (int year = 1900; year <= 2000; year++) {
            for (int month = 1; month <= 12; month++) {
                int day = year % 100 / month;
                if (day >= 1 && day <= 31) {
                    if (day * month == year % 100) {
                        System.out.println(day + "/" + month + "/" + year);
                    }
                }
            }
        }
    }
}
