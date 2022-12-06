#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

int main(){
    int t; 
    scanf("%d",&t);
    while(t--)
    {
        long n,i=2,j,pf;
        scanf("%ld",&n);
        if(n>10000)
        {
            while(i*i<=n)
            {
                while(n%i==0)
                {
                    n/=i;
                }
                i++;
            }
            printf("%ld\n",n);
        }
        else
        {
            for(j=2;j<=n;j++)
            {
                if(n%j==0)
                {
                    n/=j;
                    pf=j;
                }
            }
            printf("%ld\n",pf);
        }
    }
    return 0;
}
