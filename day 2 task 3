/*Write a program to print the below pattern:
//N should be an odd number and the value of N should be more than 4)
//Output: 
        \***** /
        *\*** /*
        **\* /**
        *** /***
        ** /*\**
        * /***\*
         /*****\
        */



// C++ code to demonstrate star pattern
#include <iostream>
using namespace std;

// Function to demonstrate printing pattern
void pypart(int n)
{
	// Outer loop to handle number of rows
	// n in this case
	for (int i = 0; i < n; i++) {

		// Inner loop to handle number of columns
		// values changing acc. to outer loop
		for (int j = 0; j < n; j++) {
      if (i==j )
    {
      cout<<"/";
    }
   else if (i+j == n-1){
    cout<< "/";
   }
    
    
    else 
			// Printing stars
			cout << "* ";
		}

		// Ending line after each row
		cout << endl;
	}
}

// Driver Function
int main()
{
	int n = 7;
	pypart(n);
	return 0;
}
