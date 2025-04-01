#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main ()
{
    printf ("\n");
    printf ("WELCOME TO THE GAME OF NUMBER GUESSING ! \n");
    printf ("\n");
    printf ("A SMALL GUIDE to the GAME : \n");
    printf ("FIRST , YOU have to DECLARE the LIMITs within which the GAME will GENERATE a RANDOM NUMBER . \n");
    printf ("THEN , YOU have to correctly GUESS that RANDOM NUMBER . \n");
    printf ("The lesser no. of TRIALS YOU make , the BETTER YOU are ! \n");
    printf ("\n");
    printf ("PRO TIP : If YOU want the LEVEL of the GAME to be DIFFICULT , then YOU can do so by DECLARING the LIMITS with a LARGE DIFFERENCE ! \n");
    printf ("ENJOY THE GAME ! \n");
    printf ("\n");
    while (1)
    {
        printf ("STARTING a NEW GAME ! \n");
        printf ("BEST OF LUCK ! \n");
        printf ("\n");
        int lower;
        printf ("PLEASE ENTER the LOWER LIMIT for this GAME : ");
        scanf ("%d" , &lower);
        int upper;
        printf ("PLEASE ENTER the UPPER LIMIT for this GAME : ");
        scanf ("%d" , &upper);
        printf ("\n");
        if (lower>upper)
        {
            printf ("Looks like YOU have made a ERROR ! \n");
            printf ("YOU have made the LOWER LIMIT more than the UPPER LIMIT . \n");
            printf ("SWAPPING the VALUES of the LIMITS to CONTINUE the GAME . \n");
            int refer = lower;
            lower = upper;
            upper = refer;
            printf ("\n");
            printf ("Hence , \n");
            printf ("The LOWER LIMIT becomes : %d \n" , lower);
            printf ("The UPPER LIMIT becomes : %d \n" , upper);
            printf ("\n");
        }
        printf ("Now moving ahead in the GAME . \n");
        printf ("\n");
        printf ("GENERATING a RANDOM NUMBER within the GIVEN LIMITS . \n");
        srand (time (0));
        int random = (rand () % (upper - lower + 1)) + lower;
        printf ("\n");
        printf ("A RANDOM NUMBER is GENERATED . \n");
        printf ("\n");
        printf ("Now YOU have to TRY to GUESS the RANDOM NUMBER that is GENERATED . \n");
        printf ("YOU have UNLIMITED TRIALS . \n");
        int trial = 1;
        while (1)
        {
            printf ("\n");
            printf ("TRIAL No. %d \n" , trial);
            int n;
            printf ("\n");
            printf ("GUESS the NUMBER : ");
            scanf ("%d" , &n);
            if (n>random)
            {
                printf ("\n");
                printf ("OOPS ! Looks like YOU have made a WRONG GUESS . \n");
                printf ("\n");
                printf ("YOU have 2 CHOICES ahead . \n");
                printf ("TYPE 1 if YOU want to EXIT the GAME . \n");
                printf ("TYPE 2 if YOU want to CONTINUE the GAME . \n");
                while (1)
                {
                    printf ("\n");
                    int choice;
                    printf ("ENTER your CHOICE : ");
                    scanf ("%d" , &choice);
                    printf ("\n");
                    if (choice==1)
                    {
                        printf ("EXITING the GAME according to your CHOICE . \n");
                        return 0;
                    }
                    else if (choice==2)
                    {
                        printf ("CONTINUING the GAME according to your CHOICE . \n");
                        break;
                    }
                    else
                    {
                        printf ("ERROR ! Your CHOICE is not according to the LIST of OPTIONS . \n");
                        printf ("CHECK the CHOICE YOU have INPUTED and RETRY again . \n");
                        continue;
                    }   
                }
                printf ("\n");
                printf ("PROVIDING YOU with a HINT before YOU RETRY again . \n");
                printf ("HINT : The GENERATED RANDOM NUMBER is LESS compared to your GUESS . \n");
                printf ("\n");
            }
            else if (n<random)
            {
                printf ("\n");
                printf ("OOPS ! Looks like YOU have made a WRONG GUESS . \n");
                printf ("\n");
                printf ("YOU have 2 CHOICES ahead . \n");
                printf ("TYPE 1 if YOU want to EXIT the GAME . \n");
                printf ("TYPE 2 if YOU want to CONTINUE the GAME . \n");
                while (1)
                {
                    printf ("\n");
                    int choice;
                    printf ("ENTER your CHOICE : ");
                    scanf ("%d" , &choice);
                    printf ("\n");
                    if (choice==1)
                    {
                        printf ("EXITING the GAME according to your CHOICE . \n");
                        return 0;
                    }
                    else if (choice==2)
                    {
                        printf ("CONTINUING the GAME according to your CHOICE . \n");
                        break;
                    }
                    else
                    {
                        printf ("ERROR ! Your CHOICE is not according to the LIST of OPTIONS . \n");
                        printf ("CHECK the CHOICE YOU have INPUTED and RETRY again . \n");
                        continue;
                    }   
                }
                printf ("\n");
                printf ("PROVIDING YOU with a HINT before YOU RETRY again . \n");
                printf ("HINT : The GENERATED RANDOM NUMBER is MORE compared to your GUESS . \n");
                printf ("\n");
            }
            else if (n==random)
            {
                printf ("\n");
                printf ("NICE ! YOU have made the RIGHT GUESS . \n");
                break;
            }
            trial++;
        }
        printf ("\n");
        printf ("CONGRATULATIONS ! \n");
        printf ("YOU have CLEARED the GAME after %d TRIALS . \n" , trial);
        printf ("\n");
        printf ("\n");
        printf ("YOU have 2 CHOICES ahead . \n");
        printf ("Type 1 if YOU want to PLAY a NEW GAME . \n");
        printf ("TYPE 2 if YOU want to EXIT the GAME . \n");
        while (1)
        {
            printf ("\n");
            int choice;
            printf ("ENTER your CHOICE : ");
            scanf ("%d" , &choice);
            printf ("\n");
            if (choice==1)
            {
                printf ("According to your CHOICE , YOU want to PLAY MORE . \n");
                printf ("RESETING the GAME . \n");
                printf ("\n");
                break;
            }
            else if (choice==2)
            {
                printf ("According to your CHOICE , YOU want to EXIT the GAME . \n");
                printf ("EXITING the GAME . \n");
                printf ("\n");
                return 0;
            }
            else
            {
                printf ("ERROR ! Your CHOICE is not according to the LIST of OPTIONS . \n");
                printf ("CHECK the CHOICE YOU have INPUTED and RETRY again . \n");
                continue;
            }
        }
    }
}
