# EX3 Write a program to count the number of digits in an integer.
## DATE:18-11-25
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1.Read the input number Take an integer num from the user.

2.Convert the number to a non-negative value Use Math.abs(num) and store it in n to handle negative numbers.

3.Check if the number is zero If n == 0, set digit count to 1 (since zero has one digit).

4.Count digits for non-zero numbers Repeatedly divide n by 10 and increment the counter until n becomes 0.

5.Display the digit count Output the total number of digits.

## Program:
```
/*
Program to to count the number of digits in an integer
Developed by: MANOJ M
RegisterNumber:  212223230122
*/
import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        int count = 0;
        int n = Math.abs(num); 

        if (n == 0) {
            count = 1; 
        } else {
            while (n > 0) {
                n /= 10; 
                count++;
            }
        }

        System.out.println("Number of digits: " + count);
    }
}
```

## Output:

<img width="787" height="326" alt="image" src="https://github.com/user-attachments/assets/2fc8b2e3-767b-428f-82e8-4feb9276056d" />


## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
