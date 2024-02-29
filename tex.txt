import java.util.Scanner;

public class ReverseNumber {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the console
        Scanner scanner = new Scanner(System.in);
        
        // Ask the user to enter a number
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();
        
        // Call the reverseNumber method to reverse the number
        int reversedNumber = reverseNumber(number);
        
        // Display the reversed number
        System.out.println("Reversed number: " + reversedNumber);
        
        // Close the scanner to avoid resource leak
        scanner.close();
    }
    
    // Method to reverse the given number
    public static int reverseNumber(int num) {
        int reversedNum = 0;
        
        // Loop through each digit of the number and reverse it
        while (num != 0) {
            int digit = num % 10;  // Extract the last digit
            reversedNum = reversedNum * 10 + digit;  // Append the digit to the reversed number
            num /= 10;  // Move to the next digit
        }
        
        return reversedNum;
    }
}
