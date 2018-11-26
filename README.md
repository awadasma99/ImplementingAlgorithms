# ImplementingAlgorithms
Practice using different array algorithms. 

    import java.util.Scanner;
    public class ImplementingAlgorithms {
      public static void main(String[] args) {
        //Copying arrays
        final int SIZE = 500;
        int[] arr1 = new int[SIZE];
        Scanner sc = new Scanner(System.in);
        int count = 0;
        //Read values into the array using a while loop.
        while (sc.hasNext() && count < SIZE) {
            arr1[count] = sc.nextInt();
            count++;
        }
        int[] arr2 = new int[arr1.length]; //makes arr 2 the same length as arr1
        for (int i = 0; i < arr1.length; i++) {
            arr2[i] = arr1[i]; //copies each value individually
        }
        //Print arrays to make sure they're the same
        System.out.print("First array: ");
        for (int i = 0; i < arr1.length; i++) {
            System.out.print(arr1[i] + " ");
        }
        System.out.print("\nSecond array: ");
        for (int i = 0; i < arr1.length; i++) {
            System.out.print(arr2[i] + " ");
        }
        System.out.println();

        //Comparing Arrays
        boolean areEqual = true;
        if (arr2.length != arr2.length) {
            System.out.println("Arrays are not equal!");
            areEqual = false;
        }
        for (int i = 0; i < arr2.length; i++) {
            if (arr2[i] != arr1[i]) {
                areEqual = false;
            }
        }

        if (areEqual)
            System.out.println("The arrays are equal!");

        else
            System.out.println("The arrays aren't equal.");

        //Searching for a key value
        int key = 3;
        for (int i = 0; i < arr1.length; i++) {
            if (arr1[i] == key) {
                System.out.println("Found key value at location " + i);
            }
        }
      }
    }
