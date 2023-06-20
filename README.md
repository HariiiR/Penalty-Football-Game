# Penalty-Football-Game

Penalty Football Game - User can play as a shooter or goalkeeper and once selected, the user can play 5 rounds and at the end of the game, both the user’s and computer’s score are returned.  For each round the computer’s chosen direction is printed to the terminal so the user knows what the computer played. Then the game asks the user for feedback as a review of the game.



PenaltyShootOutApp.Java (Main File)	This is where the game methods are defined under the class PenaltyShootOutgameapp. The GUI buttons, panels, frames, listeners etc is created under the constructer PenaltyShootOutgameapp(). Then in the main method, the “new PenaltyShootOutgameapp()” calls and starts the game and makes it visible to the user.
PlayerPosition.java	PlayerPosition is the superclass (contains the arraylist for the scores) as both shooter and goalkeeper need to store the scores. Keeps track of scores through storage in the arraylist. Some methods are overridden by the subclasses.
Shooter.java 	Shooter class inherit Playerposition. Shooter class methods overide some methods in playerposition e.g getwelcomeMessage(), getAimWord() and many more methods. A shooter has different behaviours compared to a goalkeeper that’s why the methods are overridden from the superclass PlayerPosition.
Goalkeeper.java 	Shooter class inherits Playerposition (which overrides some methods in playerposition e.g getwelcomeMessage(), getAimWord() and many more methods. A goalkeeper has different behaviours compared to a shooter that’s why the methods are overridden from the superclass PlayerPosition.
RandomNumber.java	RandomNumber class has a static method which generates random numbers and these numbers are taken as the computer’s input for the game.
WindowCloser.java	This allows the user to press the X button which closes the GUI window and ends the program.


The game (PenaltyShootOutGameApp.java) first displays the shooter and goalkeeper buttons, and the user can select what the user wants to be. If the user chooses shooter, an object of shooter is created for the user (Shooter.java) and an object of goalkeeper is created for the computer (GoalKeeper.java). (All Shooter and Goalkeeper objects created in this game has superclass reference (PlayerPosition.java.)) The user can practice taking penalties by using the (left / centre/ right) buttons against the computer (the computer dives using the RandomNumber class method). However, if the user chooses goalkeeper, an object of goalkeeper is created for the user (GoalKeeper.java) and an object of Shooter is created for the computer (Shooter.java), and the user has to save the computer’s shots (computer’s shots use the RandomNumber class method) by using the (left / centre/ right) buttons. In each round if the user saves/shoots the goal (depending on what the user chooses to be), the user’s score will be shown. At the end of the game, all scores are returned, and the user will see a feedback button and once pressed the user will be asked to rate the game out of 10 and they also must input their name. The program makes sure that the user enters a number equal to 10 or below and only it makes sure that the user can only enter or integers otherwise an error message will be shown to the user. When the user submits their name and rating, the information will be written in the txt File IO (Part 1). The user also has the option to see the feedback stored in the txt file where they can see their feedback being stored there too File IO (Part 2)




Example of one round in the game
Where the user is the shooter and the goalkeeper is the computer, the user gets to choose where to shoot by pressing one of the buttons (left / center/ right). The goalkeeper is controlled by the random number generator so if the computer produces a right (3) and the user presses right (3), the shot will not go in. A point of 1 will added to the computer’s scores.

Polymorphism in the game
The user (playerOne) and computer (playerTwo) both have a reference to the object type of superclass (PlayerPosition).  Dynamic Binding shown under the Shooter button listener and Goalkeeper button listener (in PenaltyShootOutApp.java) where the methods for playerOne and playerTwo are decided during runtime as the methods are overridden from the superclass as they have unique behaviours. The methods that is run for playerOne and playerTwo is dependent on the user's decision to either be a shooter or goalkeeper. For example, if the user presses the shooter button then the user (playerOne)  will be created as an object of Shooter and computer (playerTwo) will created as an object of GoalKeeper. Basically, playerOne can be Shooter or Goalkeeper and playerTwo can be Shooter or Goalkeeper and we do not know which one it is until runtime. playerOne cannot be Shooter when playerTwo is Shooter same goes for Goalkeeper.

Running the program in the terminal
Compile all java files. Then do the line below to run it.
java PenaltyShootOutApp.java



Please email me at h.ravindiran@se20.qmul.ac.uk if you have any questions about the game 

