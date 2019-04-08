# Main

/* 
	Title of Project: Attendance Checker
	
	Names:
	Johannes Dalogdog
	Dominick Ondiano
	Kent Delgado
	
	Second Semester Project
*/




import java.util.Scanner;

public class Main {
	
	public static void main(String args[]) {
		
		Records r = new Records();     //Scanner connected to case Records
		Scanner sc = new Scanner(System.in);
		boolean exit = false;
		System.out.println("This program is allowed to check events whenever a student is Present, Late, and Absent");//welcoming message
		System.out.println("This register and regulates the student on it's presence about the said Event X.");
		System.out.println("Welcome to Attendance checker for Event X! Please do the following: ");
		while(!exit) {
			System.out.println("Type '1' - register a student");
			System.out.println("Type '2' - display all students");
			System.out.println("Type '3' - delete a student");
			System.out.println("Type '4' - check attendance");
			System.out.println("Type '5' - exit program");

			String choice = sc.nextLine();
			System.out.println();
			
			switch(choice) {
			
			case "1":    //case 1 is registering the student or we could say profiling
				System.out.println("Enter student name (Last name, First name, Middle initial");
				String n = sc.nextLine();
				System.out.println("Enter school name (acronyms are acceptable)");
				String s = sc.nextLine();
				r.register(n,s);
				System.out.println();
				break;
				
			case "2":    //case 2 is the display of student whenever the presence on the said event
				r.displayAll();
				System.out.println();
				break;
			case "3":    //case 3 is where we delete the students name
				System.out.println("Enter student name");
				String del = sc.nextLine();
				r.delete(del);
				break;
			case "4":    //case 4 is checking the attendance
				r.checkAttendance();
				break;
			case "5":   //case 5 is exit
				System.exit(0);
			}
		}
	}
	
	
}
