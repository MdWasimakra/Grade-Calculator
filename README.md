# Grade-Calculator

 import java.util.Scanner;
    public class gardecalculator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter the number of subjects: ");
        int numSubjects = scanner.nextInt();
        
        double totalScore = 0;
        for (int i = 1; i <= numSubjects; i++) {
            System.out.print("Enter the score for subject " + i + ": ");
            double score = scanner.nextDouble();
            totalScore += score;
        }
        
        double averageScore = totalScore / numSubjects;
        System.out.println("Average grade: " + averageScore);
        
        // Determine grade based on average score
        char grade;
        if (averageScore >= 90) {
            grade = 'A';
        } else if (averageScore >= 80) {
            grade = 'B';
        } else if (averageScore >= 70) {
            grade = 'C';
        } else if (averageScore >= 60) {
            grade = 'D';
        } else {
            grade = 'F';
        }
        
        System.out.println("Grade: " + grade);
        
        scanner.close();
    }
}
