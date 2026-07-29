//Write a program to print whether a number is even or odd, also take input from the user
import java.util.Scanner;

public class EvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        System.out.println((num % 2 == 0) ? "Even" : "Odd");

        sc.close();
    }
}
output
Enter a number: 4
Even
//Take name as input and print a greeting message for that particular name.
import java.util.Scanner;

public class Greeting {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.println("Hello, " + name + "! Welcome.");

        sc.close();
    }
}
output
Enter your name: pavan
Hello, pavan! Welcome.
//Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.without any codition
import java.util.Scanner;

public class SimpleInterest {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter Principal (P): ");
        double P = sc.nextDouble();

        System.out.print("Enter Time (T): ");
        double T = sc.nextDouble();

        System.out.print("Enter Rate (R): ");
        double R = sc.nextDouble();

        double SI = (P * T * R) / 100;

        System.out.println("Simple Interest = " + SI);

        sc.close();
    }
}
output
Enter Principal (P): 5000
Enter Time (T): 
2
Enter Rate (R): 
8
Simple Interest = 800.0
//Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        double num1 = sc.nextDouble();

        System.out.print("Enter second number: ");
        double num2 = sc.nextDouble();

        System.out.print("Enter operator (+, -, *, /): ");
        char op = sc.next().charAt(0);

        switch (op) {
            case '+':
                System.out.println("Result = " + (num1 + num2));
                break;

            case '-':
                System.out.println("Result = " + (num1 - num2));
                break;

            case '*':
                System.out.println("Result = " + (num1 * num2));
                break;

            case '/':
                System.out.println("Result = " + (num1 / num2));
                break;

            default:
                System.out.println("Invalid Operator");
        }

        sc.close();
    }
}
output
Enter first number: 5
Enter second number: 6
Enter operator (+, -, *, /): *
Result = 30.0
//Take 2 numbers as input and print the largest number.
import java.util.Scanner;

public class LargestNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int num1 = sc.nextInt();

        System.out.print("Enter second number: ");
        int num2 = sc.nextInt();

        int largest = Math.max(num1, num2);

        System.out.println("Largest number = " + largest);

        sc.close();
    }
}
output
Enter first number: 2
Enter second number: 3
Largest number = 3
//Input currency in rupees and output in USD.
import java.util.Scanner;

public class RupeesToUSD {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter amount in Rupees: ");
        double rupees = sc.nextDouble();

        double usd = rupees / 83.50;

        System.out.println("Amount in USD = $" + usd);

        sc.close();
    }
}
output
Enter amount in Rupees: 1000000
Amount in USD = $11976.047904191617
//To calculate Fibonacci Series up to n numbers.
import java.util.Scanner;

public class FibonacciSeries {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of terms: ");
        int n = sc.nextInt();

        int a = 0, b = 1;

        System.out.print("Fibonacci Series: ");
        for (int i = 0; i < n; i++) {
            System.out.print(a + " ");

            int c = a + b;
            a = b;
            b = c;
        }

        sc.close();
    }
}
output

Enter number of terms: 8
Fibonacci Series: 0 1 1 2 3 5 8 13 
//To find out whether the given String is Palindrome or not.
import java.util.Scanner;

public class StringPalindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a String: ");
        String str = sc.nextLine();

        String reverse = new StringBuilder(str).reverse().toString();

        String result = str.equals(reverse) ? 
                "The given String is a Palindrome" : 
                "The given String is not a Palindrome";

        System.out.println(result);

        sc.close();
    }
}
output
Enter a String: pavan
The given String is not a Palindrome
Enter a String: level
The given String is a Palindrome
//To find Armstrong Number between two given number.
import java.util.Scanner;

public class ArmstrongNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter starting number: ");
        int start = sc.nextInt();

        System.out.print("Enter ending number: ");
        int end = sc.nextInt();

        System.out.println("Armstrong numbers are:");

        for (int num = start; num <= end; num++) {
            int temp = num;
            int sum = 0;
            int digits = String.valueOf(num).length();

            while (temp > 0) {
                int rem = temp % 10;
                sum = sum + (int)Math.pow(rem, digits);
                temp = temp / 10;
            }

            String result = (sum == num) ? String.valueOf(num) : "";
            System.out.println(result);
        }

        sc.close();
    }
}
output
Enter starting number: 2
Enter ending number: 10
Armstrong numbers are:
2
3
4
5
6
7
8
9
