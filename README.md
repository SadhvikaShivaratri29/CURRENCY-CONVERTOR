# CURRENCY-CONVERTOR
import java.util.Scanner;

public class CurrencyConverter {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Exchange rates (as of today's rates)
        final double USD_TO_EUR = 0.91;
        final double USD_TO_GBP = 0.81;
        final double USD_TO_JPY = 110.29;

        System.out.println("Welcome to Currency Converter!");

        // Input amount in USD
        System.out.print("Enter amount in USD to convert: ");
        double usdAmount = scanner.nextDouble();

        // Conversion options
        System.out.println("Choose currency to convert to:");
        System.out.println("1. EUR");
        System.out.println("2. GBP");
        System.out.println("3. JPY");
        System.out.print("Enter your choice (1, 2, or 3): ");
        int choice = scanner.nextInt();

        double convertedAmount = 0;

        // Perform conversion based on user choice
        switch (choice) {
            case 1:
                convertedAmount = usdAmount * USD_TO_EUR;
                System.out.printf("%.2f USD$ is equal to %.2f EUR\n", usdAmount, convertedAmount);
                break;
            case 2:
                convertedAmount = usdAmount * USD_TO_GBP;
                System.out.printf("%.2f USD$ is equal to %.2f GBP\n", usdAmount, convertedAmount);
                break;
            case 3:
                convertedAmount = usdAmount * USD_TO_JPY;
                System.out.printf("%.2f USD$ is equal to %.2f JPY\n", usdAmount, convertedAmount);
                break;
            default:
                System.out.println("Invalid choice. Please choose 1, 2, or 3.");
        }

        scanner.close();
    }
}
