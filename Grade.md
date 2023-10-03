# Grade
Letter grade
import java.util.*;
public class LetterGrade
{
    public static void main(String[]args)
    {
        Scanner console = new Scanner(System.in);
        System.out.println("What is your name?\nMy name is ");
        String name = console.nextLine();
        double grade = calculateAvg();
        System.out.printf("Student's name: %s\nStudent's average: %-6.2f\n",name,grade);
        printLetter(grade);
    }
    public static double calculateAvg(){
        Scanner console = new Scanner(System.in);
        System.out.println("Enter your 3 scores:");
        double total = 0;
        for (int i=1; i <= 3; i++){
            System.out.println("Enter a value");
            total = total + console.nextDouble();
        }
        return total / 3;
    }
    public static char letterGrade( double grade){
        System.out.print("Your Grade is: ");
        char letter = ' ';
        if(grade>=90 && grade<=100)
        {
            letter = 'A';
            System.out.print(letter);
        }
        else if(grade>=80 && grade<90)
        {
            letter = 'B';
           System.out.print(letter);
        } 
        else if(grade>=70 && grade<80)
        {
            letter = 'C';
            System.out.print(letter);
        }
        else if(grade>=60 && grade<70)
        {
            letter = 'D';
            System.out.print(letter);
        }
        else if(grade>=0 && grade<60)
        {
            letter = 'F';
            System.out.print(letter);
        }
        return letter;
        }
    }
