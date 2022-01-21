/*  Given a string s, find the length of the longest substring without repeating characters.*/
#include <bits/stdc++.h>

using namespace std;

// Function to find and print longest substring without repeating characters.
string longestSubstring(string s)
{
	int i;
	int strLenght = s.length();

	// starting point of current substring.
	int first = 0;

	// length of current substring.
	int subStrLen;

	// maximum length substring 
	int maxlen = 0;

	// starting index of maximum length substring.
	int start;

	// Hash Map to store last occurrence of repeated character.
	unordered_map<char, int> pos;

	// repeated first character is index 0;
	pos[s[0]] = 0;

	for (i = 1; i < strLenght; i++) {

		// If this character is not present in hash, then this is first occurrence of this character, store this in hash.
		if (pos.find(s[i]) == pos.end())
			pos[s[i]] = i;

		else {
			// If this character is present in hash then this character has previous occurrence,  check if that is before or after starting point of current substring.
			if (pos[s[i]] >= first) {

				// check length of this substring
				subStrLen = i - first;
				if (maxlen < subStrLen) {
					maxlen = subStrLen;
					start = first;
				}

				// Next substring will start after the last encounter
				first = pos[s[i]] + 1;
			}

			// Update last encounter of  character.
			pos[s[i]] = i;
		}
	}

	// Compare length of last substring with maxlen
	if (maxlen < i - first) {
		maxlen = i - first;
		start = first;
	}

	//return the longest Substring
	return s.substr(start, maxlen);
}


int main()
{
	string s;
  cout<<"Enter the string ";
  cin>> s;
	cout << "The answer is '"<< longestSubstring(s)<<"' with the length of "<<longestSubstring(s).length();
	return 0;
}
