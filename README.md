import java.util.Scanner;

public class TwoDArray {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int rows, cols;

        // Get the number of rows from the user with input validation.
        do {
            System.out.print("Enter the number of rows (positive integer): ");
            while (!scanner.hasNextInt()) {
                System.out.println("Invalid input. Please enter a positive integer.");
                scanner.next();
            }
            rows = scanner.nextInt();
        } while (rows <= 0);


        // Get the number of columns from the user with input validation.
        do {
            System.out.print("Enter the number of columns (positive integer): ");
            while (!scanner.hasNextInt()) {
                System.out.println("Invalid input. Please enter a positive integer.");
                scanner.next();
            }
            cols = scanner.nextInt();
        } while (cols <= 0);


        // Create and initialize the 2D array.
        int[][] array2D = new int[rows][cols];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                array2D[i][j] = i * j;
            }
        }

        // Print the array.
        System.out.println("The 2D array is:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.printf("%4d", array2D[i][j]); // %4d formats the output to occupy 4 spaces.
            }
            System.out.println(); // New line after each row.
        }

        scanner.close();
    }
}
