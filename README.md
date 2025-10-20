# Elevate-Lab-Task-1-Calculator
// **It Is Console Based Calculator which is used to calculate +, -,*,/  and also pow of numbers .**


import java.util.Scanner;
public class Calculator{
    public static void addition(Scanner sc){
        System.out.print("Enter First Number :-");
        double a = sc.nextDouble();
        System.out.print("Enter Second Number :-");
        double b = sc.nextDouble();
        System.out.println("Result :- "+(a+b));
    }
    public static void substraction(Scanner sc){
        System.out.print("Enter First Number :-");
        double a = sc.nextDouble();
        System.out.print("Enter Second Number :-");
        double b = sc.nextDouble();
        System.out.println("Result :- "+(a-b));

    }
    public static void multiplication(Scanner sc){
        System.out.print("Enter First Number :-");
        double a = sc.nextDouble();
        System.out.print("Enter Second Number :-");
        double b = sc.nextDouble();
        System.out.println("Result :- "+(a*b));

    }
    public static void division(Scanner sc){
        System.out.print("Enter First Number :-");
        double a = sc.nextDouble();
        System.out.print("Enter Second Number :-");
        double b = sc.nextDouble();
        if(b!=0){
        System.out.println("Result :- "+(a/b));
        }
        else{
            System.out.println("Error: Division By Zero is not allowed.");
        }

    }
    public static void power(Scanner sc){
        System.out.print("Enter Base Number :-");
        double a = sc.nextDouble();
        System.out.print("Enter Exponent Number :-");
        double b = sc.nextDouble();
        System.out.println("Result :- "+Math.pow(a, b));

    }
    public static void main(String[] args){
         Scanner sc = new Scanner(System.in);
         System.out.println("HELLO WELCOME TO MY CALCULATOR :- ");
         while(true){
            int choice;
            System.out.println("Type 1 for Calculation and AnyNumber for Exit :- ");
              try{
                choice = sc.nextInt();
             }
         catch(Exception e){
            System.out.println("InValid Number please Enter Only a Number eg. 1 or 2,3");
            sc.nextLine();
            continue;
         }
        
         if(choice!=1){
             break;
        }
        
            System.out.println("Enter + for Addition ");
            System.out.println("Enter - for Subtraction ");
            System.out.println("Enter * for Multiplication ");
            System.out.println("Enter / for Division ");
            System.out.println("Enter ^ for Power");

            char ch = sc.next().charAt(0);
            switch (ch) {
                case '+':
                    addition(sc);
                    break;
                case '-':
                    substraction(sc);
                    break;
                case '*':
                    multiplication(sc);
                    break;
                case '/':
                    division(sc);
                    break;
                case '^':
                    power(sc);
                    break;
                default:
                    System.out.println("Invalid Operator ! please enter valid operator.");
            }
          
         }
         sc.close();;
    }
}
