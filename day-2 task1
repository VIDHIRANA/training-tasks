/* Write a program to remove duplicate values from an array and returns an array of unique values. int[] removeDuplicates(int[]values) */



// considering that the array may not be sorted 
#include "iostream"
#include "unordered_map"
using namespace std;

void removeDuplicate(int arr[], int numOfElements)
{
	// using Hash map to store the elements which are repeating
	unordered_map<int, bool> mp;

	for (int i = 0; i < numOfElements; ++i) {

    // display the unique
		if (mp.find(arr[i]) == mp.end()) {
			cout << arr[i] << " ";
		}

		// Insert the element in the hash map
		mp[arr[i]] = true;
	}
}

int main()
{
	int arr[] = { 9, 2, 5, 1, 7, 2, 4, 2 };
	int numOfElements = sizeof(arr) / sizeof(arr[0]);
	removeDuplicate(arr, numOfElements);
	return 0;
}
