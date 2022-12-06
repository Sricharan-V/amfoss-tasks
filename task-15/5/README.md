#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

long lcm(long a, long b)
{
    long i,lcm;
    if(a>b)
    {
        for(i=a;i<=a*b;i++)
        {
            if(i%a==0 && i%b==0)
            {
                lcm=i;
                break;
            }
        }
    }
    else
    {
        for(i=b;i<=a*b;i++)
        {
            if(i%b==0 && i%a==0)
            {
                lcm=i;
                break;
            }
        }
    }
    return lcm;
}

int main(){
    int t; 
    scanf("%d",&t);
    while(t--)
    {
        long n,i,x=1; 
        scanf("%ld",&n);
        for(i=1;i<=n;i++)
        {
            x=lcm(x, i);
        }
        printf("%ld\n",x);
    }
    return 0;
}
