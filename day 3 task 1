//Write a method Boolean isValidSudoku(int[][]Sudoku) Returns true if the given Sudoku is correctly arranged otherwise false
//Determine if a 9 x 9 Sudoku board is valid. Only the filled cells need to be validated according to the following rules:
//1.Each row must contain the digits 1-9 without repetition.
//2.Each column must contain the digits 1-9 without repetition.
//3.Each of the nine 3 x 3 sub-boxes of the grid must contain the digits 1-9 without repetition.




// sudoku is valid or not
#include <bits/stdc++.h>
using namespace std;

// Checks for any repeatation in row or not
bool checkRow(char Arr[9][9], int row)
{
	// store the char encountered 
	set<char> check;

	for (int i = 0; i < 9; i++) {

		// If seen before, return false
		if (check.find(Arr[row][i]) != check.end())
			return false;

		// If not an empty, put value in set
		if (Arr[row][i] != '.')
			check.insert(Arr[row][i]);
	}
	return true;
}
// similar to row check for col
// Checks for any repeatation in col or not
bool checkCol(char Arr[9][9], int col)
{
	set<char> check;

	for (int i = 0; i < 9; i++) {

		// If seen before, return false
		if (check.find(Arr[i][col]) != check.end())
			return false;

		//If not an empty, put value in set
		if (Arr[i][col] != '.')
			check.insert(Arr[i][col]);
	}
	return true;
}
// similar to row and col check for 3x3 boxes 

//  Checks for any repeatation in  3x3 box or not.
bool inBox(char Arr[9][9], int inRow, int inCol)
{
	set<char> check;

	for (int row = 0; row < 3; row++) {
		for (int col = 0; col < 3; col++) {
			char box = Arr[row + inRow][col + inCol];

			// If seen before, return false
			if (check.find(box) != check.end())
				return false;

			//If not an empty, put value in set
			if (box != '.')
				check.insert(box);
		}
	}
	return true;
}

// check all 3 conditions 
bool isValid(char Arr[9][9], int row, int col)
{
	return checkRow(Arr, row) && checkCol(Arr, col) &&
		inBox(Arr, row - row % 3, col - col % 3);
}

bool isValidSudoku(char Arr[9][9], int n)
{
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < n; j++) {

			// If one or more is not satisfied return false 
			if (!isValid(Arr, i, j))
				return false;
		}
	}
	return true;
}

// Drivers code
int main()
{
	char sudoku[9][9] = { { '5', '3', '.', '.', '7', '.', '.', '.', '.' },
						{ '6', '.', '.', '1', '9', '5', '.', '.', '.' },
						{ '.', '9', '8', '.', '.', '.', '.', '6', '.' },
						{ '8', '.', '.', '.', '6', '.', '.', '.', '3' },
						{ '4', '.', '.', '8', '.', '3', '.', '.', '1' },
						{ '7', '.', '.', '.', '2', '.', '.', '.', '6' },
						{ '.', '6', '.', '.', '.', '.', '2', '8', '.' },
						{ '.', '.', '.', '4', '1', '9', '.', '.', '5' },
						{ '.', '.', '.', '.', '8', '.', '.', '7', '9' } };

	if (isValidSudoku(sudoku, 9)){
    cout << "TRUE";
  }
  else{
    cout << " False";
  }
	return 0;
}
