#include <math.h>  
#include <stdio.h>  
#include <string.h>  
#include <stdlib.h>  
#include <assert.h>  
#include <limits.h>  
#include <stdbool.h>  
  
int main()  
{  
    (&emsp)long long int t;  
    scanf("%lld",&t);  
    while(t--)  
    {  
        long long int n,x,a,b,c;  
        scanf("%lld",&n);  
        a=(n-1)/3;  
        b=(n-1)/5;  
        c=(n-1)/15;  
        x=3*(a*(a+1))/2 + 5*(b*(b+1))/2 - 15*(c*(c+1))/2;  
        printf("%lld\n",x);  
    }  
    return 0;  
}
