PRINTING PATTERN:
3

54

876

1211109

876

54

3

PREREQUISITE:
Basic knowledge of C language and use of loops.

ALGORITHM:
Take the number of rows as input from the user and store it in any variable.(‘r‘ in this case).
Run a loop ‘r’ number of times to iterate through each of the rows. From i=0 to i<r. The loop should be structured as for( i=0 ; i<r : i++).
Use an if condition to to print the top half of the pyramid. if (i<=r/2). Then intialise count=count1 and Then run a loop from j=0 to j<=i. The loop should be structured as for(j=0 ; j<=i ; j++)
Inside this loop increment count.
Outside this loop initialise count1=count.
Then run a loop from j=0 to j<=i. The loop should be structured as for(j=0 ; j<=i ; j++)
Inside this loop decrement count and then print it
Outside the loop print a newline
Else
Run a different loop from j=i to j<r. The loop should be structured as for( j=i ; j<r ; j++).
Inside this loop decrement count and then print it.
Inside the main loop print a newline to move to the next line after each row is printed.
CODE IN C:
#include<stdio.h>
int main()
{
int i,j,r,count,count1;
count1=3;                              //declaring integer variables i,j for loops , r for number of rows and count for increment in value
count=0;                              //initialising count
printf("Enter the number of rows(odd) :\n"); //Asking user for input
scanf("%d",&r);                       //taking number of rows and saving it in variable r
for(i=0;i<r;i++)                      // loop for number of rows
  {
    if(i<=r/2)                       //if condition for top half
      {
        count=count1;                //copying value
        for(j=0;j<=i;j++)            // loop for digits per each row
          {
             count++;                //incrementing count

          }
        count1=count;                //copying value
        for(j=0;j<=i;j++)            // loop for digits per each row
          {
             count--;                //incrementing count
             printf("%d",count);     //printing digits
          }

       printf("\n");                  // printing newline after each row

      }
    else
      {
        for(j=i;j<r;j++)              //loop for lower half
          {
            count--;                  //decrementing count
            printf("%d",count);       //printing digits
          }
        printf("\n");                 //printing newline
      }

  } 

}
TAKING INPUT:DISPLAYING OUTPUT:
