# Ex2 Count how many times a number appears in an array recursively.
## DATE:18-11-25
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1.Read the value of n, input n elements into array arr, and read the number key whose occurrences must be counted. 

2.Call the recursive function countOccurrences(arr, n, 0, key) starting from index 0.

3.Inside the recursive function, check if the current index equals n;if yes, return 0 because the entire array has been checked. 

4.If arr[index] equals key, return 1 + countOccurrences(arr, n, index + 1, key);otherwise return countOccurrences(arr, n, index + 1, key).

5.Return the final count to the main program and print how many times key appears in the array.

## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: MANOJ M
RegisterNumber:  212223230122
*/
import java.util.Scanner;

public class CountOccurrencesRecursive {
    
    public static int countOccurrences(int[] arr, int n, int index, int key) {
        if (index == n) {
            return 0; 
        }
        if (arr[index] == key) {
            return 1 + countOccurrences(arr, n, index + 1, key);
        } else {
            return countOccurrences(arr, n, index + 1, key);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

    
        int n = sc.nextInt();

        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int key = sc.nextInt();

        int count = countOccurrences(arr, n, 0, key);

        System.out.println("The number " + key + " appears " + count + " time(s) in the array.");
    }
}
```

## Output:

<img width="705" height="414" alt="image" src="https://github.com/user-attachments/assets/6cfd7bb1-efd7-4a7f-9e08-f7c0d50028a7" />


## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
