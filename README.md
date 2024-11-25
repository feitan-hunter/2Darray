import java.util.Scanner;

public class TwoDArray {

    public static void main(String[] args) {
         Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the number of rows: ");
        int rows = scanner.nextInt();
        
        System.out.print("Enter the number of columns: ");
        int col = scanner.nextInt();

        int[][] array = new int[rows][col];

        System.out.println("Populating the 2D array with i * j values:");
        for (int i = 0 i < rows; i++) {
            for (int j = 0; j < col; j++) {
                array[i][j] = i * j;
            }
        }

        System.out.println("\nThe populated 2D array (product of row and column) is:");
        for (int i = 0; i < rows; i++) 
            for (int j = 0; j < col; j++) {
                System.out.print(array[i][j] + "\t");
            }
            System.out.println();
        }

        scanner.close();
    }
}
