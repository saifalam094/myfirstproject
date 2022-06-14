# My first project is guessing number game which is totally based on c language. 
The source code of this game are as follows:
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main()
{

    int number;
    int guess;
    int nguessed = 1;
    srand(time(0));
    number = rand() % 100 + 1;
    printf("the number is %d\n",number);
    do
    {
        printf("guess the number between 1 to 100\n");
        scanf("%d", &guess);
        if (guess > number)
        {
            printf("lower number please\n");
        }
        else if(guess < number)
        {

            printf("higher number please\n");
        }

        else
        {
            printf("you guessed the number in %d attempt\n", nguessed);
        }
        nguessed++;
    }

    while (guess != number);
    return 0;
}
