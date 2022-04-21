#include<iostream>
#include<stdio.h>
#include<ctype.h>
using namespace std;
	int main(){
		char c;
		int i = 0 , lc = 0 , uc = 0 , dig = 0 , ws = 0 , pun = 0 , oth = 0;
		
		cout << " Please Enter a character string and then press ENTER: ";
		
		// Analyse text as it is input 
		while ( ( c = getchar( ) ) != '\n' ) {
			if ( islower ( c ) ){
				lc++;
			}
			else if ( isupper ( c ) ) {
				uc++;
			}
			else if ( isdigit ( c ) ) {
				dig++;
			}
			else if ( isspace ( c ) ) {
				ws++;
			}
			else if ( ispunct ( c ) ) {
				pun++;
			}
			else {
				oth++;
			}
		}
		// display the content of different types of character 
		
		cout << " You Typed : " << '\n';
		cout << " lower case letters = " << lc << '\n';
		cout << " Upper case letters = " << uc << '\n';
		cout << " Digits = " << dig << '\n';
		cout << " White space = " << ws << '\n';
		cout << " Punctuation = " << pun << '\n';
		cout << " Other = " << oth << '\n';
		
		return 0;
	}
