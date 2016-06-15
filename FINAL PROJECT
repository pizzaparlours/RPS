/* Audrey Aurelia, 1126340, Computer Programming 11
* FINAL PROJECT - Learning Java
* Rock Paper Scissors Game
* note: when you type something invalid, the loop is still a bit wonky, i couldn`t figure out how to reset the value again :(
* other note: i used Eclipse to run this program!
* June 15, 2016
*/
import java.util.Scanner;
import java.util.Random;

public class Main {
   public static void main (String[] args) {
      Scanner keyboard = new Scanner(System.in);

      String computer, user; //sets up the strings that will be used
      char keepPlaying; 

      do { // similar to a while loop, but guarantees to execute it once 
         
    	 computer = computerChoice(); //sets the comp variables 
         user = userChoice(); //sets the user variable

         System.out.println("The computer chose " + computer);
         System.out.println("You chose " + user);

         determineWinner(computer, user); //goes to the determineWinner void

         while (computer.equals(user)) { //what happens if both chose the same one, they have to play again
         
            computer = computerChoice(); //goes to computerChoice to set computers variable
            user = userChoice(); //goes to userChoice to set the users variable

            System.out.println("The computer choice " + computer);
            System.out.println("You chose " + user);
            determineWinner(computer, user); //goes to determineWinner again
         }


         System.out.println("\n" + "Would you like to play again? (y/n)"); //asks user if they would like to play again
         keepPlaying = keyboard.nextLine().toLowerCase().charAt(0); //automatically lower cases the value user types in and sets it as the variable

         while ( keepPlaying != 'y' && keepPlaying != 'n' ) {
            System.out.println("Invalid input, please enter (y/n)"); //what happens if there is an invalid input
            keepPlaying = keyboard.nextLine().toLowerCase().charAt(0);
         }

      } while (keepPlaying == 'y'); //loops the whole thing over again to start game
   }
   
  
   public static String computerChoice() {
      String[] choice = {"rock","paper","scissors"};
      Random rand = new Random();
      int computerChoice = rand.nextInt(3); //computer chooses one randomly
      return choice[computerChoice]; //return the choice
   }
   
   public static String userChoice() {
      Scanner keyboard = new Scanner(System.in);
      System.out.print("Enter rock, paper, or scissors: ");
      String choice = keyboard.nextLine();

      isValidChoice(choice); //if they type something else, goes to isValidChoice boolean
      return choice;
   }
   
   
   public static boolean isValidChoice (String choice) { //what happens if they type something else
      Scanner keyboard = new Scanner(System.in);

      while (!(choice.equalsIgnoreCase("rock")) && !(choice.equalsIgnoreCase("paper")) && !(choice.equalsIgnoreCase("scissors"))) {
       System.out.print("Invalid input, enter rock, paper, or scissors: "); 
       choice = keyboard.nextLine();
      }

       return true;
    }
   
   
    public static void determineWinner(String computer, String user) { //all the various possibilities
       if (computer.equalsIgnoreCase("rock") && user.equalsIgnoreCase("paper"))
          System.out.println("\n" + "Paper wraps rock.\nYou`ve Won!!");
       else if (computer.equalsIgnoreCase("rock") && user.equalsIgnoreCase("scissors"))
          System.out.println("\n" + "You lose. Rock smashes scissors.\nThe computer wins!");
       else if (computer.equalsIgnoreCase("paper") && user.equalsIgnoreCase("rock"))
          System.out.println("\n" + "You lose. Paper wraps rock.\nThe computer wins!");
       else if (computer.equalsIgnoreCase("paper") && user.equalsIgnoreCase("scissors"))
          System.out.println("\n" + "Scissors cuts paper.\nYou`ve Won!");
       else if (computer.equalsIgnoreCase("scissors") && user.equalsIgnoreCase("rock"))
          System.out.println("\n" + "Rock smashes scissors.\nYou`ve Won!");
       else if (computer.equalsIgnoreCase("scissors") && user.equalsIgnoreCase("paper"))
          System.out.println("\n" + "You lose. Scissors cuts paper.\nThe computer wins!");
       else if (computer.equalsIgnoreCase(user))
          System.out.println("\n" + "The game is tied!\nGet ready to play again...");
    }   
}
