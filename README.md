#include <cs50.h>
#include <stdio.h>

long get_correct_card(void);                            //hint for the function to be used

int main(void)                                          //main function
{
    long number = get_correct_card();

    int und_add, nund_add;
    und_add = 0;
    nund_add = 0;


    if (340000000000000 < number && number < 350000000000000)               //check for AMEX cards starting w/ 34
    
    {
        long n;
        n = number;
        int in_und = 0; int in_non = 0;
        for (int index = 0; index <= 14; index ++)
        {
            int und_term = (index % 2);
            
            
            int und_rem, und_rem_2_ad, und_rem_2, und_rem_2_rem1, und_rem_2_rem2;
            int rem;
            int non_rem, non_rem_ad;
            
            if (und_term != 0)
            {
                und_rem = (n % 10);
                und_rem_2 = und_rem * 2;
                rem = und_rem;
                
                if(und_rem_2 > 9)
                {
                    und_rem_2_rem1 = (und_rem_2 % 10);
                    und_rem_2_rem2 = (und_rem_2 - und_rem_2_rem1) / 10;
                    und_rem_2_ad = (und_rem_2_rem1 + und_rem_2_rem2);
                }
                
                else
                {
                    und_rem_2_ad = und_rem_2;
                }
                
                in_und += und_rem_2_ad;
                
            }
            else
            {
                non_rem = (n % 10);
                rem = non_rem;
                in_non += non_rem;
            }
            
            n = (n - rem) / 10;
        }
        int total = (in_und + in_non);
        int div_10 = (total % 10);
        if (div_10 == 0)
        {
            printf("AMEX\n");
        }
        else
        {
            printf("INVALID\n");
        }
    }
    
    else if (370000000000000 < number && number < 380000000000000)                      //check for AMEX cards starting w/ 37
    {
        long n;
        n = number;
        int in_und = 0; int in_non = 0;
        for (int index = 0; index <= 14; index ++)
        {
            int und_term = (index % 2);
            
            
            int und_rem, und_rem_2_ad, und_rem_2, und_rem_2_rem1, und_rem_2_rem2;
            int rem;
            int non_rem, non_rem_ad;
            
            if (und_term != 0)
            {
                und_rem = (n % 10);
                und_rem_2 = und_rem * 2;
                rem = und_rem;
                
                if(und_rem_2 > 9)
                {
                    und_rem_2_rem1 = (und_rem_2 % 10);
                    und_rem_2_rem2 = (und_rem_2 - und_rem_2_rem1) / 10;
                    und_rem_2_ad = (und_rem_2_rem1 + und_rem_2_rem2);
                }
                else
                {
                    und_rem_2_ad = und_rem_2;
                }
                in_und += und_rem_2_ad;
            }
            else
            {
                non_rem = (n % 10);
                rem = non_rem;
                in_non += non_rem;
            }
            
            n = (n - rem) / 10;
        }
        int total = (in_und + in_non);
        int div_10 = (total % 10);
        if (div_10 == 0)
        {
            printf("AMEX\n");
        }
        else
        {
            printf("INVALID\n");
        }
    }
    
    else if (5100000000000000 < number && number < 5600000000000000)                //check for MASTERCARD
    {
        long n;
        n = number;
        int in_und = 0; int in_non = 0;
        for (int index = 0; index <= 15; index ++)
        {
            int und_term = (index % 2);
            
            
            int und_rem, und_rem_2_ad, und_rem_2, und_rem_2_rem1, und_rem_2_rem2;
            int rem;
            int non_rem, non_rem_ad;
            
            if (und_term != 0)
            {
                und_rem = (n % 10);
                und_rem_2 = und_rem * 2;
                rem = und_rem;
                
                if(und_rem_2 > 9)
                {
                    und_rem_2_rem1 = (und_rem_2 % 10);
                    und_rem_2_rem2 = (und_rem_2 - und_rem_2_rem1) / 10;
                    und_rem_2_ad = (und_rem_2_rem1 + und_rem_2_rem2);
                }
                else
                {
                    und_rem_2_ad = und_rem_2;
                }
                in_und += und_rem_2_ad;
            }
            else
            {
                non_rem = (n % 10);
                rem = non_rem;
                in_non += non_rem;
            }
            
            n = (n - rem) / 10;
        }
        int total = (in_und + in_non);
        int div_10 = (total % 10);
        if (div_10 == 0)
        {
            printf("MASTERCARD\n");
        }
        else
        {
            printf("INVALID\n");
        }
    }
    
    else if (4000000000000 < number && number < 5000000000000)              //checking 13 digit VISA cards
    {
        long n;
        n = number;
        int in_und = 0; int in_non = 0;
        for (int index = 0; index <= 14; index ++)
        {
            int und_term = (index % 2);
            
            
            int und_rem, und_rem_2_ad, und_rem_2, und_rem_2_rem1, und_rem_2_rem2;
            int rem;
            int non_rem, non_rem_ad;
            
            if (und_term != 0)
            {
                und_rem = (n % 10);
                und_rem_2 = und_rem * 2;
                rem = und_rem;
                
                if(und_rem_2 > 9)
                {
                    und_rem_2_rem1 = (und_rem_2 % 10);
                    und_rem_2_rem2 = (und_rem_2 - und_rem_2_rem1) / 10;
                    und_rem_2_ad = (und_rem_2_rem1 + und_rem_2_rem2);
                }
                else
                {
                    und_rem_2_ad = und_rem_2;
                }
                in_und += und_rem_2_ad;
            }
            else
            {
                non_rem = (n % 10);
                rem = non_rem;
                in_non += non_rem;
            }
            
            n = (n - rem) / 10;
        }
        int total = (in_und + in_non);
        int div_10 = (total % 10);
        if (div_10 == 0)
        {
            printf("VISA\n");
        }
        else
        {
            printf("INVALID\n");
        }
    }
    
    else if (4000000000000000 < number && number < 5000000000000000)                //checking 16 digit VISA cards
    {
        long n;
        n = number;
        int in_und = 0; int in_non = 0;
        for (int index = 0; index <= 15; index ++)
        {
            int und_term = (index % 2);
            
            
            int und_rem, und_rem_2_ad, und_rem_2, und_rem_2_rem1, und_rem_2_rem2;
            int rem;
            int non_rem, non_rem_ad;
            
            if (und_term != 0)
            {
                und_rem = (n % 10);
                und_rem_2 = und_rem * 2;
                rem = und_rem;
                
                if(und_rem_2 > 9)
                {
                    und_rem_2_rem1 = (und_rem_2 % 10);
                    und_rem_2_rem2 = (und_rem_2 - und_rem_2_rem1) / 10;
                    und_rem_2_ad = (und_rem_2_rem1 + und_rem_2_rem2);
                }
                else
                {
                    und_rem_2_ad = und_rem_2;
                }
                in_und += und_rem_2_ad;
            }
            else
            {
                non_rem = (n % 10);
                rem = non_rem;
                in_non += non_rem;
            }
            
            n = (n - rem) / 10;
        }
        int total = (in_und + in_non);
        int div_10 = (total % 10);
        if (div_10 == 0)
        {
            printf("VISA\n");
        }
        else
        {
            printf("INVALID\n");
        }
    }

    else
    {
        printf("INVALID\n");
    }
}




long get_correct_card(void)                             // getting a correct card number
{
    long number;
    do
    {
        number= get_long("Number: ");
    }
    while (number < 0);
    return number;
}
