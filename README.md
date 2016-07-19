# dragon-game
package Intro;

import java.util.Scanner;

public class lab2 {
	public static void main(String[] args) {
		
		Scanner scan1 = new Scanner(System.in);
		
		int state = 1;
		boolean play = true;
		String name = "";
		String option;
		
		
	
		while(play==true) {
			switch(state){
			case 1:
				System.out.println("Welcome! What's your name: ");
				name = scan1.nextLine(); 
				System.out.println("Hello " + name);
				System.out.println("Would you like to play a game? yes/no: ");
				option =scan1.nextLine(); 
				if (option.equalsIgnoreCase ("yes"))
					state = 2;
				else
					play = false;
			case 2: 
				System.out.println("Excellent! You are walking across a field and you encounter a fire-breathing dragon! What would you do? (enter face the beast or run away)");
				option =scan1.nextLine();
				if (option.equalsIgnoreCase ("face the beast"))
					state = 3;
				else
					play = false;
			
			case 3: 
				System.out.println("Armed with your bow and arrow, you approach the dragon. It stares at you withs its ____ eyes. (enter red or blue)");
				option = scan1.nextLine();
				if(option.equalsIgnoreCase("Red"))
					System.out.println("You are able to slay the dragon and walk away a Hero");
				else
					System.out.println("Oh no you were eaten, Game over!");
				break;
				
				
			
		} play = false;
		}
		System.out.println("Goodbye!");
	}

}
