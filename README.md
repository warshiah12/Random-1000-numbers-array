# Random-1000-numbers-array
#using array &amp; rand() function
#include<iostream>
#include<algorithm>
using namespace std;
int main()
{
	int num[1000], count = 0,search;
	char cont;
		cout << "Enter the number you want to search: ";
		cin >> search;
		while (cin.fail() || search < 0 || search >100)    
		{
			cout << "\aInvalid Command! " << endl;
			cout << "Please enter the number again from 1-100: ";
			cin.clear();
			cin.ignore();
			cin >> search;
		}
		for (int j = 0; j < 1000; j++)
		{
			num[j] = rand() % 100;      //using 100% to make sure numbers are not too big
			cout << num[j] << endl;
			if (num[j] == search) {     
				count++;
			}
		}
		cout << search << " appeared " << count << " times " << endl;
	return 0;

}
