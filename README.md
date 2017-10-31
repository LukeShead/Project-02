# Project-2

## The code that I created the game for is below:

#include <ctime> // allows the use of time to be implemented
#include <cstdlib> // opens a library
#include <iostream>
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



# The IDE and implementation

### The IDE I used was repl.it

 This was a very good IDE to use as it allowed me to run my code easily and let me debug my code easier through the intergrated
 debugger that it provides, with this I was able to solve problems much more effieciently than if I was using a platform like notepad. 
 With this, I was able to create the game much easier than normal. Being able to have a IDE that knew the code I was using and offered syntax highlighting, this made things a lot easier to learn the code and allowing myself to have a neater code so it was easier to read as well as having a better understanding at what parts of the code did and what was connected to them.
 
 ### Coding standards I use
 
 My coding standards have not changed from what they where from the first project, I use tabs to help organize my code to make sure that it is easy to read. I place any of the code that is associated with a function further out than the function, this is because as I read left to right, I can look at the functions clearly then look at what they do after I have found the function that I was looking for.
