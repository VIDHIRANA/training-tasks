/* Find the largest number less than N whose each digit is prime number */


#include <bits/stdc++.h>
using namespace std;

// check if the digit is prime no or not 
bool isPrime(char c)
{
	return (c == '2' || c == '3' || c == '5' || c == '7');
}

// if the no is not a prime no then replace with previous prime character
void decrease(string& s, int i)
{
	
	if (s[i] <= '2') {
		s.erase(i, 1);
		s[i] = '7';
	}

	else if (s[i] == '3')
		s[i] = '2';
	else if (s[i] <= '5')
		s[i] = '3';
	else if (s[i] <= '7')
		s[i] = '5';
	else
		s[i] = '7';

	return;
}

string primeDigits(string s)
{
	for (int i = 0; i < s.length(); i++) {

		// find first non prime char
		if (!isPrime(s[i])) {

			// find first char greater than 2
			while (s[i] <= '2' && i >= 0)
				i--;

			if (i < 0) {
				i = 0;
				decrease(s, i);
			}

			
			else
				decrease(s, i);

			// replace remaining with 7
			for (int j = i + 1; j < s.length(); j++)
				s[j] = '7';		

			break;
		}
	}

	return s;
}


int main()
{
	string s = "57575766";
	cout << primeDigits(s) << endl;

	
	return 0;
}
