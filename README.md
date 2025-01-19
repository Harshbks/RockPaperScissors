# RockPaperScissors
its a game which i love the most , that's why i am creating .
#include <math.h>
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
 
// Function to implement the game
int game(char harsh , char computer)
{
    // If both the harsh and computer
    // has choose the same thing
    if (harsh == computer)
        return -1;
 
    // If harsh's choice is stone and
    // computer's choice is paper
    if (harsh == 's' && computer == 'p')
        return 0;
 
            // If harsh's choice is paper and
            // computer's choice is stone
            else if (harsh == 'p' && computer == 's') return 1;
 
    // If harsh's choice is stone and
    // computer's choice is scissor
    if (harsh == 's' && computer == 'z')
        return 1;
 
    // If harsh's choice is scissor and
    // computer's choice is stone
    else if (harsh == 'z' && computer == 's')
        return 0;
 
    // If harsh's choice is paper and
    // computer's choice is scissor
    if (harsh == 'p' && computer == 'z')
        return 0;
 
    // If harsh's choice is scissor and
    // computer's choice is paper
    else if (harsh == 'z' && computer == 'p')
        return 1;
}
 
// Driver Code
int main()
{
    // Stores the random number
    int n;
 
    char harsh, computer, result;
 
    // Chooses the random number
    // every time
    srand(time(NULL));
 
    // Make the random number less
    // than 100, divided it by 100
    n = rand() % 100;
 
    if (n < 33)
 
        computer = 's';
 
    else if (n > 33 && n < 66)
 
        computer = 'p';
 
    else
        computer = 'z';
 
    printf("\n\n\n\n\t\t\t\tEnter s for STONE, p for PAPER and z for SCISSOR\n\n\t\t\t\t\t\t\t");
 
     printf("ENTER : ") ; scanf("%c", &harsh);
 
    result = game(harsh , computer);
 
    if (result == -1) {
        printf("\n\n\t\t\t\tGame Draw!\n\n");
    }
    else if (result == 1) {
        printf("\n\n\t\t\t\tWow! harsh have won the game!\n\n");
    }
    else { 
        printf("\n\n\t\t\t\tOh! harsh have lost the game!\n\n");
    }
        printf("\t\t\t\tYou choose : %c and Computer choose : %c\n\n",harsh, computer);
 
    return 0; }
