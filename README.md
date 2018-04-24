# Project-02.

## About the project.

Project 02 was to build a higher or lower card game similar to the old game show, the user is shown a card then asked to pick whether the next will be of a higher or lower value than the card. After choosing the card will be shown to the user, with this the card is checked to see whether it is higher or lower and either give points if they are correct or give a game over if it's incorrect. 

## Planning the Project.

When planning the project I took into consideration the scope of the project and all of the user's needs and wants, I made user stories for the project that could help me with planning it right. I used a flowchart to understand exactly how the program would work and with it, this allowed me to look at the individual tasks within and decompose the project. By having this I was able to plan the objectives of this project easily. By having the individual tasks within the project, I was able to effectivly manage my time to each project, I used a Gantt chart to show all of my time with each individual point, most of them were small however having this time gave me a schedule to keep to, therefore it was very helpful to create one.

With this project, I made note of all points within it, this includes what the project brief said, with just asking to create a higher or lower game and saying nothing else, I checked about the quality standards of the project, since it was a broad project, it meant that quality could be increased at certain points but it would not be any different from having the simple project standards in the project being complete, with this is mind I cut down on time by having the task be done to the requirements and not risk nto completing it trying to overcomplicate things.

This program is an event driven program, this is because it waits for an input before it runs the rest of the code, without anything being typed by the user, the program does not run, this makes it an event driven program. In order for it to be a procedural program it would need to run on its own and not require any other inputs. There are no objects that can be interacted with within this program and as of such it cannot be known as an object orientated program. 

When looking at other versions of higher or lower card games, the source code of the programs were heavily based around bein event-driven, mine was the same as this when completed however the code of these more proffesional programs were much more complicated having the code constantly running numbers and having the program allow the user to have the same number and not just higher and lower. The code was neat and had a simplistic standard, this was very helpful to decide how my program would run.

The project was done in C++, this is because the language has an easier method of implementing the right algorithm for my project, for this project I needed it to be event-driven, this meant having the code only continue once there was input, because of this it means that the coding language I used needed to be suitable, and for this C++ was the right one. The language allowed me to add the correct functions easily as the type of algorithm that I wanted to implement and the language style work well together in order to make it easier for me to create. This is why I used C++.

## Process I followed to build the application

In order to build this application, the process had to follow a certain development cycle, with this project I used an agile development plan, this was done by making constant prototypes, with this I was able to constantly improve my project. When building an application, it is through certain steps, the planning is the most important step and shows how the app will work along with how it will be built. The development stage is where it is all created and this is where my development cycle was used however it can be any form of cycle. After this it is the testing and evaluation stage, this is the testing stage and looking at the application as a whole whilst evaluating the project and project performance. This is the stage I evaluated all of my work on and how the project went.

# FlowChart
![Flow](https://github.com/LukeShead/Project-02/blob/master/Flow%20proj2.PNG)

## The code that I created the game for is below:
``` cpp

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

```

# The IDE and implementation.

### The IDE I used was repl.it.

This was a very good IDE to use as it allowed me to run my code easily and let me debug my code easier through the intergrated
debugger that it provides, with this I was able to solve problems much more effieciently than if I was using a platform like notepad. 
With this, I was able to create the game much easier than normal. Being able to have a IDE that knew the code I was using and offered syntax highlighting, this made things a lot easier to learn the code and allowing myself to have a neater code so it was easier to read as well as having a better understanding at what parts of the code did and what was connected to them.

#### Screenshot of IDE
![ide](https://github.com/LukeShead/Project-02/blob/master/IDE.PNG)
 
 ### Coding standards I use.
 
#### Ease of reading- tabs for spacing, line positioning.
My coding standards have not changed from what they where from the first project, I use tabs to help organize my code to make sure that it is easy to read. I place any of the code that is associated with a function further out than the function, this is because as I read left to right, I can look at the functions clearly then look at what they do after I have found the function that I was looking for. This helped me keep track of what functions did what and what lines belonged to, this allowed me to work faster when developing and testing the code, it also made debugging the code much easier as I was easily able to show what lines had the errors and the functions they belonged to, having this allowed me to only look at what was wrong and not the entire code.

#### Variable Names
When using variables I keep all of the names simple and easily identifiable, for example a variable for a card generator will be called "CGEN" so that I will be able to look at the variable and see the simplified version of the function name. This allows me and other people to be able to look at my code and see exactly what variable links too and what it does, this will be done with all variables as it also helps make the code look neater as it allows the code to be shorter and when defining variable names, it can be done with the lines being smaller so that the functions can be in focus instead of the variable names.


### Debugging.

As I said before my coding standard helped me debug more effectively and become more aware of the problems in my code a lot faster than I could do originally before using notepad and not having my coding standard before made it more difficult to debug problems, however using repl.it I was able to detect what the computer did not understand and find a solution to the error quickly. When debugging the errors I would look at the lines of code that the computer did not understand, most of the time it would be a variable that would be mispelt or me forgetting a at the end of a line, these errors the debugger would tell me what was wrong with them. 

### Debugging process
The process of debugging is all about testing, the testing of a program can happen in many ways and many teams may use different methods in order to debug their program successfully. When testing the code, the IDE would have its own debugging process by showing what it couldnt understand, other IDE's will have different ways of doing this. However the teams process, debugging is the most important process within a programs development as bugs within a program can stop it from completing it's function and therefore not be successful in its purpose.

However, there were occasions to which the computer did not understand the code because of reasons that were further along with the code with them either not being written right or having functions that overlapped, this was solved by seeing what the code did, then looking at what was associated with it. By successfully debugging my code I was able to complete my assignment as the debugger would help my development by telling me what was wrong with my code.

I would run the program after a few lines of code or a function was completed, this would be to help me understand what part of my code was working and what part was not. For the parts that wasn't working the debugger would help me locate the small errors so that they would not overlapp with others and end up making the code difficult to debug. This is why the debugger was very useful for my project

### IDE's and how they help with debugging.

When creating a program, many people use normal text editors in order to allow them to have complete control over what they build, however this method of programming is not very useful for debugging, this is because the bugs in a system are usually not clearly highlighted when testing the code. This can make debugging the programming much more difficult, to remove this problem, people use IDE's to help them design and create programs as well as run and test them, this is because of the features that it can provide, for example many IDE's provide a syntax colouring which allows for easier reading as the user can see what parts of code are functions or variables. 

IDE's will use it's own debugging devices in order to help developers test their code, this is usually done within the IDE by running the code within it, the IDE will usually have a section devoted to showing the parts of the code that it cannot understand. IDE's will not show what's wrong with the code but what it cannot understand, this means that parts of the code that have the bug within them can be found easier as the part it cannot understand will be linked to the bug somewhere in the code. For example if a variable name is mispelt it will say that it cannot understand what the mispelt variable is, this means the developer will be able to know that the variable is the problem and therefore can debug it easier. 

IDE's provide a multitude of tools and techniques that can help with debugging when building and testing code, this can come from the IDE giving help to the user write the code or through the testing. One example of a feature that helps is the ability to use the three different techniques, one of them is step-over, this is the action of an IDE to not run a certain function or subroutine but skip it in order to run another subroutine, this can be used to help test different parts of code without testing all of it.








