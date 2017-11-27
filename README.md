# Project-02.

## About the project.

Project 02 was to build a higher or lower card game similar to the old game show, the user is shown a card then asked to pick whether the next will be of a higher or lower value than the card. After choosing the card will be shown to the user, with this the card is checked to see whether it is higher or lower and either give points if they are correct or give a game over if it's incorrect. 

## Planning the Project.

When planning the project I took into consideration the scope of the project and all of the user's needs and wants, I made user stories for the project that could help me with planning it right. I used a flowchart to understand exactly how the program would work and with it, this allowed me to look at the individual tasks within and decompose the project. By having this I was able to plan the objectives of this project easily. By having the individual tasks within the project, I was able to effectivly manage my time to each project, I used a Gantt chart to show all of my time with each individual point, most of them were small however having this time gave me a schedule to keep to, therefore it was very helpful to create one.

With this project, I made note of all points within it, this includes what the project brief said, with just asking to create a higher or lower game and saying nothing else, I checked about the quality standards of the project, since it was a broad project, it meant that quality could be increased at certain points but it would not be any different from having the simple project standards in the project being complete, with this is mind I cut down on time by having the task be done to the requirements and not risk nto completing it trying to overcomplicate things.

![Flow] (https://raw.githubusercontent.com/LukeShead/Project-02/master/Capture.PNG)

## The code that I created the game for is below:

#include <ctime> // allows the use of time to be implemented
#include <cstdlib> // opens a library
#include <iostream> // This allows for standard input and output
// all of the includes such as ctime and iostream all have different purposes

using namespace std; // allows me to use code such as cout without having the std:: before.



int card() { // function for the random number to be generated in. Put above the main so the computer can regognize it when it hits main.

  int val;
  val = (rand() % 13 )+ 1;  // This is what gets the random number, % 13 + 1 is 1-13.

    return val;  // This is what returns the value from the function val.
}

// Main is the first function to be run, in order to get from other functions you must put them above the main. (main function is mandatory for C++)
int main() {
  
    srand(time(NULL)); // I use srand time as it is a constantly changing number and it can be used to keep the numbers random.
    int card1 = card(); // retrieves the result of card as card 1.
    cout << "HIGHER OR LOWER GAME!!! \n";
	  cout << card1; 
	  cout << "\n";
		char highorlow;
		cout << "H for Higher, L for Lower: "; // this prints the text in the brackets.
		cin >> highorlow; // this is the input of the user
		cout << "\n"; //separates the lines of code above and below.
		int card2 = card(); // retrieves the result of card as card 2
    cout << card2; // This retrieves the result that card1 is returning.
    
    int prize; // this is te function that gives the prize to the player.
    int bal;
    bal = 0;
    
    
    if ((highorlow == 'H' && card1 > card2 )|| // this is showing if the number is higher than the first.
        (highorlow == 'L' && card1 < card2)){ // this is showing if the number is lower than the first
          
          cout << "\nIncorrect, sorry but...You lose"; // This is the message that will display if the player is wrong
        
        }
        else {
          cout << "\nYou Win!!!! Thats £100 added to your pool.\n"; // This is the message that will display if the player is right
          prize = bal + 100; // this is the amount of money that the player gets.
          cout << prize; // This is where the prize is printed.
        }        
return 0;

}



# The IDE and implementation.

### The IDE I used was repl.it.

This was a very good IDE to use as it allowed me to run my code easily and let me debug my code easier through the intergrated
debugger that it provides, with this I was able to solve problems much more effieciently than if I was using a platform like notepad. 
With this, I was able to create the game much easier than normal. Being able to have a IDE that knew the code I was using and offered syntax highlighting, this made things a lot easier to learn the code and allowing myself to have a neater code so it was easier to read as well as having a better understanding at what parts of the code did and what was connected to them.
 
 ### Coding standards I use.
 
My coding standards have not changed from what they where from the first project, I use tabs to help organize my code to make sure that it is easy to read. I place any of the code that is associated with a function further out than the function, this is because as I read left to right, I can look at the functions clearly then look at what they do after I have found the function that I was looking for. This helped me keep track of what functions did what and what lines belonged to, this allowed me to work faster when developing and testing the code, it also made debugging the code much easier as I was easily able to show what lines had the errors and the functions they belonged to, having this allowed me to only look at what was wrong and not the entire code.

### Debugging.

As I said before my coding standard helped me debug more effectively and become more aware of the problems in my code a lot faster than I could do originally before using notepad and not having my coding standard before made it more difficult to debug problems, however using repl.it I was able to detect what the computer did not understand and find a solution to the error quickly. When debugging the errors I would look at the lines of code that the computer did not understand, most of the time it would be a variable that would be mispelt or me forgetting a ; at the end of a line, these errors the debugger would tell me what was wrong with them. However, there werer occasions to which the computer did not understand the code because of reasons that were further along with the code with them either not being written right or having functions that overlapped, this was solved by seeing what the code did, then looking at what was associated with it. By successfully debugging my code I was able to complete my assignment.
