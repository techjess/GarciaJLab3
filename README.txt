# Lab_3
Instructions for lab 3

CPSC 121
Lab 3
Fall 2018
Eric May
Printing Shapes
Create a program that:
1.  Prompt the user to choose between a rectangle and a triangle
2.  Prompt user for shape parameters
      a)  Rectangle
        Ask user to choose between supplying a word or a width
        Ask user for height
      b)  Triangle
        Ask user to choose between supplying a word or a width, and whether the triangle points up or down
        Read input
3.  Ask the user whether they want to print to a file, “myshape.txt”, or to cout
4.  Print the desired shape
5.  Ask the user if they would like to exit, or return to step 1

Any input requested from the user should only be one character in length per decision.

Points:
2 - Documentation, readability, format
2 - Proper program flow (conditionals, loops, etc)
1 - File output
1 - Functions
2 - Filename and Header
2 - Output testing

Header
//<Your Name>
//CPSC 121 Lab 3
//<MM/DD/YY>

Filename
<Last Name><First Initial>lab3.cpp
For example, my assignment would be named MayElab3.cpp

---

Submission
This project will not be submitted through TITANium, but rather through Github. Make sure you're in our organization, 
https://github.com/CSUF-s18-121-05-15 , and name it similarly to the name you used for your cpp file where applicable. If you are unable to due to not 
being a member of the organization, please return to Titanium and fill out the survey available.

Use this invitation link for submission: https://classroom.github.com/g/yRNJZxG2


Functions provided as reference; you do NOT need to use functions in this program, although it is allowed.

//void DrawRectangle(int width, int height);
//DrawRectangle(5,3)
*****
*****
*****

//void DrawRectangle(string word, int height);
//DrawRectangle("VOTE", 3)
shape.txt:
VOTE
VOTE
VOTE

//void DrawTriangle(int size, bool pointingUp);
//DrawTriangle(4, true)
*
**
***
****

//void DrawTriangle(string word, bool pointingUp);
//DrawTriangle("VOTE", false)
VOTE
OTE
TE
E

//DrawTriangle("VOTE", true)
E
TE
OTE
VOTE

