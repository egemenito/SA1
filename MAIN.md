import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter number of students:");
        int n = sc.nextInt();
        sc.nextLine();

        Student[] students = new Student[n];

        for (int i = 0; i < n; i++) {
            System.out.println("Enter name:");
            String name = sc.nextLine();

            System.out.println("Enter faculty number:");
            int facNumber = sc.nextInt();

            System.out.println("Enter grade:");
            double grade = sc.nextDouble();
            sc.nextLine();

            students[i] = new Student(name, facNumber, grade);
        }

        System.out.println("Students who passed the exam:");

        for (int i = 0; i < n; i++) {
            if (students[i].grade >= 3) {
                students[i].printInfo();
            }
        }

        sc.close();
    }
}
