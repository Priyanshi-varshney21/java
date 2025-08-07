//ques 1(* Write a program to Print "Welcome To Java ". *)
public class Welcome {
    public static void main(String[] args) {
        System.out.println("Welcome To Java");
    }
}

//ques 2 WAP to print your address i) using single print ii) using multiple println
public class PrintAddress {
    public static void main(String[] args) {
        System.out.println(
            "123, Green Street\n" +
            "Apt 45B\n" +
            "Gurugram, Haryana\n" +
            "India"
        );
    }
}
//Using multiple System.out.println(...) calls
public class PrintAddress {
    public static void main(String[] args) {
        System.out.println("123, Green Street");
        System.out.println("Apt 45B");
        System.out.println("Gurugram, Haryana");
        System.out.println("India");
    }
}
//ques 3 WAP to print addition of 2 numbers (with Scanner)
public class AddTwoNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int num1 = sc.nextInt();

        System.out.print("Enter second number: ");
        int num2 = sc.nextInt();

        sc.close();

        int sum = num1 + num2;
        System.out.println("Sum = " + sum);
    }
}
// ques 4 Write a program in Java to design simple calculator for (+, -, *, and /) using switch case
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first number: ");
        double a = sc.nextDouble();
        System.out.print("Enter second number: ");
        double b = sc.nextDouble();
        System.out.print("Choose operator (+, -, *, /): ");
        char op = sc.next().charAt(0);

        switch (op) {
            case '+': System.out.println("Result: " + (a + b)); break;
            case '-': System.out.println("Result: " + (a - b)); break;
            case '*': System.out.println("Result: " + (a * b)); break;
            case '/': 
                if (b != 0) System.out.println("Result: " + (a / b)); 
                else System.out.println("Cannot divide by zero");
                break;
                default: System.out.println("Invalid operator");
        }
    }
}
// ques 5 WAP that reads a number in meters converts it to feet and displays the result
import java.util.Scanner;

public class MeterToFeet {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter distance in meters: ");
        double meters = sc.nextDouble();
        double feet = convertMetersToFeet(meters);
        System.out.printf("%.2f meters = %.4f feet\n", meters, feet);
        sc.close();
    }

    public static double convertMetersToFeet(double meters) {
        // Multiply by the conversion factor
        return meters * 3.28084;  // 1 meter ≈ 3.28084 feet :contentReference[oaicite:0]{index=0}
    }

//ques 6
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner=new Scanner(System.in);
        
        System.out.print("Enter the value of a: ");
        double a=scanner.nextDouble();
        
        System.out.print("Enter the value of b: ");
        double b=scanner.nextDouble();
        
        System.out.print("Enter the value of c: ");
        double c=scanner.nextDouble();
        
        double discriminant=b*b-4*a*c;
        
        if(discriminant<0){
            System.out.println("There will be no real solutions");
        }
        else if(discriminant==0){
            double solution=-b/(2*a);
            System.out.println("There will be one real solution which is :"+solution);
        }
        else{
            double solution1 = (-b + Math.sqrt(discriminant)) / (2 * a);
            double solution2 = (-b - Math.sqrt(discriminant)) / (2 * a);
            System.out.println("There will be two real solutions: "+solution1+" and "+solution2);
        }
        scanner.close();
    }
}
