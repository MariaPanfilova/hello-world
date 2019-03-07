# hello-world
repository_0

Live long and prosper!

From far beyond the galaxies I've jorneyed to this place
To study the behaviour patterns of the human race.
And I find them
Hihgly illogical

#include <stdio.h>
#include <stdlib.h>
struct integer
{
	int n;
	int *A;
};
typedef struct integer N;

int COM_NN_D (N a, N b) // a- первый массив b-второй массив n-размерность первого m-размерность второго
{
    int i, res,t, count;
    t=1;
    count=0;
    if (a.n>b.n) res=2;
    if (a.n<b.n) res=1;
    if (a.n==b.n)
    {
        for (i=a.n-1; i>=0, t!=0; i--)
        {
            if (a.A[i]>b.A[i])
            {
                res=2;
                t=0;
            }
            else if (a.A[i]<b.A[i])
            {
                res=1;
                t=0;
            }
            else count++;
        }
    if (count==a.n) res=0;
    }

    return res;
}

int main ()
{
    N a, b;
    int c,d,i;
    printf("Enter sizes: ");
    scanf("%d %d", &a.n, &b.n);
    printf("Enter a: ");
    scanf("%d", &c);
    a.A = (int*)calloc(a.n,sizeof(int));
    i = 0;
    while(c > 0)
    {
        a.A[i] = c % 10;
        c = c / 10;
        i++;
    }
    for(i = a.n-1; i >=0 ; i--)
    {
        printf("%d ", a.A[i]);
    }
    puts("");
    printf("Enter b: ");
    scanf("%d", &c);
    b.A = (int*)calloc(b.n,sizeof(int));
    i = 0;
    while(c > 0)
    {
        b.A[i] = c % 10;
        c = c / 10;
        i++;
    }
    for(i = b.n-1; i >= 0; i--)
    {
        printf("%d ", b.A[i]);
    }
    puts("");
    printf("Result: %d", COM_NN_D(a,b));
    return 0;
}
