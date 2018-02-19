//Jesse Garcia
//CPSC 121
//2/11/18

#include<iostream>
#include<string>
using namespace std;

void rectangleWidth(int w, int h) {
	for (int i = 0;i < h;i++) {
		for (int j = 0;j < w;j++) {
			cout << "*";
		}
		cout << endl;
	}
}

void rectangleWord(int s, int h, string w) {

	for (int i = 0;i < h;i++){ // outer 
		for (int j = 0;j < s;j++) //inner
		{
			cout << w[j]; // value that is output
		}
		cout << endl;//new line for next line output
	}
}



void triangleWordUp(int s,string w) {
		for (int i = 0;i < s;i++) // outer  height
		{
			for (int j = 0;j <= i;j++) //inner width
			{
				cout << w[j]; // value that is output
			}
			cout << endl;//new line for next line output
		}
	
}

void triangleWordDown(int s, string w) {
	for (int i = s;i > 0;i--) // outer  height
	{
		for (int j = 0;j < i;j++) //inner width
		{
			cout << w[j]; // value that is output
		}
		cout << endl;//new line for next line output
	}
}

void triangleWidthUp(int w) {
	for (int i = 1;i <= w;i++) // outer  height
	{
		for (int j = 1;j <= i;j++) //inner width
		{
			cout << "*"; // value that is output
		}
		cout << endl;//new line for next line output
	}
}

void triangleWidthDown(int w) {
	for (int i = w;i >= 1;i--) // outer  height
	{
		for (int j = 1;j <= i;j++) //inner width
		{
			cout << "*"; // value that is output
		}
		cout << endl;//new line for next line output
	}
}

int main()
{

	char loop = 'y';
	while (loop == 'y') {
		char answer = 'z';
		cout << "Please choose between: a) rectangle or b)triangle\n ";
		cin >> answer;
		//Square pattern
		char squareAnswer = 'x';

		int width = 0;
		int height = 0;
		string word = "";
		//If answer is a square
		if (answer == 'a') {

			cout << "Would you like to supply: a)word or b)width? \n";
			cin >> squareAnswer;
			if (squareAnswer == 'a') {
				cout << "Please give us your word: ";
				cin >> word;
			}
			else {
				cout << "Please give us a width: ";
				cin >> width;
			}
			cout << "Please give us a height: ";
			cin >> height;


			//If the user chose a rectangle, word

			if (squareAnswer == 'a') {
				int size = word.length();
				rectangleWord(size, height, word);
			}
			//Rectangle , width
			else {
				rectangleWidth(width, height);
			}

		}
		//Triangle
		else {
			
			int triangle;
			int triWidth;
			string triWord = "";
			char triAnswer = 'x';
			char triDirection = 'z';

			cout << "Would you like to provide: a)word or b)width? ";
			cin >> triAnswer;
			cout << "Would you like the trianlgle to point: a)up or b)down? ";
			cin >> triDirection;
			
			//Triangle with user providing word
			if (triAnswer == 'a') {
				cout << "Please provide word: ";
				cin >> triWord;
				int size = triWord.length();
				
				//pointing up, word
				if (triDirection == 'a') {
					triangleWordUp(size, triWord);
				}

				//pointing down, word
				else {
					triangleWordDown(size, triWord);
				}

			}






			//Triangle with user providing width
			else {
				cout << "Please provide width: ";
				cin >> triWidth;
				//Pointing UP, width
				if (triDirection == 'a') {
					triangleWidthUp(triWidth);
				}
				//Pointing Down, width
				else {
					triangleWidthDown(triWidth);
				}
			}
		}



		cout << "Hit 'y' to try again. Otherwise, hit any key to exit: \n";
		cin >> loop;
		

	}
	system("pause");
	return 0;

}


