import java.time.YearMonth;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите номер месяца (1-12): ");
        int month = scanner.nextInt();

        if (month < 1 || month > 12) {
            System.out.println("Некорректный номер месяца. Введите число от 1 до 12.");
        } else {
            YearMonth yearMonth = YearMonth.of(YearMonth.now().getYear(), month);
            int daysInMonth = yearMonth.lengthOfMonth();
            System.out.println("Количество дней в указанном месяце: " + daysInMonth);
        }
        
        scanner.close();
    }
}





2
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите положительное число: ");
        int number = scanner.nextInt();

        // Проверяем, что число положительное
        if (number <= 0) {
            System.out.println("Вы ввели некорректное число. Пожалуйста, введите положительное число.");
        } else {
            int sum = calculateDigitSum(number);
            System.out.println("Сумма цифр числа " + number + " равна: " + sum);
        }

        scanner.close();
    }

    public static int calculateDigitSum(int number) {
        int sum = 0;

        // Используем цикл для вычленения цифр числа и их суммирования
        while (number != 0) {
            sum += number % 10;
            number /= 10;
        }

        return sum;
    }
}


3
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите температуру в градусах Цельсия: ");
        double celsius = scanner.nextDouble();

        double fahrenheit = celsiusToFahrenheit(celsius);
        System.out.println("Температура в градусах Фаренгейта: " + fahrenheit);

        double convertedCelsius = fahrenheitToCelsius(fahrenheit);
        System.out.println("Обратно переведенная температура в градусах Цельсия: " + convertedCelsius);

        scanner.close();
    }

    public static double celsiusToFahrenheit(double celsius) {
        return celsius * 9/5 + 32;
    }

    public static double fahrenheitToCelsius(double fahrenheit) {
        return (fahrenheit - 32) * 5/9;
    }
}








