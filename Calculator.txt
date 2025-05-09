import java.util.Scanner;

public class GentlemensCalculator {

    public static void main(String[] args) {
        Scanner inkwell = new Scanner(System.in);
        System.out.println("══════════════════════════════════════");
        System.out.println("     Welcome, Esteemed User, to the");
        System.out.println("      Gentlemen’s Arithmetical Engine");
        System.out.println("══════════════════════════════════════");

        System.out.print("Kindly enter the first numeral: ");
        double a = inkwell.nextDouble();

        System.out.print("Please select an operation (+, -, *, /): ");
        char operation = inkwell.next().charAt(0);

        System.out.print("Do enter the second numeral: ");
        double b = inkwell.nextDouble();

        double result = 0;
        boolean valid = true;

        switch (operation) {
            case '+':
                result = a + b;
                break;
            case '-':
                result = a - b;
                break;
            case '*':
                result = a * b;
                break;
            case '/':
                if (b == 0) {
                    System.out.println("Oh dear! Division by nought is unbecoming.");
                    valid = false;
                } else {
                    result = a / b;
                }
                break;
            default:
                System.out.println("That symbol is not part of Her Majesty’s mathematics.");
                valid = false;
        }

        if (valid) {
            System.out.println("══════════════════════════════════════");
            System.out.println(" Result of your noble computation: " + result);
            System.out.println("══════════════════════════════════════");
        }

        System.out.println("Thank you for using the Gentlemen’s Calculator.");
        System.out.println("May your equations always balance.");
    }
}
