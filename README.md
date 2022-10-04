# the-block-game
New repository
QUES=The citizens of Byteland regularly play a game. They have blocks each denoting some integer from 0 to 9. These are arranged together in a random manner without seeing to form different numbers keeping in mind that the first block is never a 0. Once they form a number they read in the reverse order to check if the number and its reverse is the same. If both are same then the player wins. We call such numbers palindrome.

Ash happens to see this game and wants to simulate the same in the computer. As the first step he wants to take an input from the user and check if the number is a palindrome and declare if the user wins or not. 


#include <stdio.h>

int main(void) {
	int t,n,r,a,rev=0;
	scanf("%d", &t);
    while(t--){
        rev=0;
	    scanf("%d", &n);
	 a=n;
	while(n!=0){
	    r=n%10;//remender
	    rev=r+rev*10;//reverse
	    n=n/10;
	}
    
	if(rev==a){
	    printf("wins\n");//if number=reverse
	}
	else{
	    printf("loses\n");//if number!=reverse
	}
    }
	return 0;
}
