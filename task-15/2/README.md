#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

int main(){
    long long int t;
    scanf("%lld",&t);
    while(t--)
    {
        long long int n,a=1,b=1,temp,sum=0;
        scanf("%lld",&n);
        while(a+b<=n)
        {
            temp=a;
            a=b;
            b=a+temp;
            if(b%2==0)
            sum=sum+b;
        }
        printf("%lld\n",sum);
    }
return 0;
}
