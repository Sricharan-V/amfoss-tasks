#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

long pal(long num)
{
    long temp=num,sum=0,temp2,ret;
    temp2=temp;
    while(temp>0)
    {
        sum=sum*10+temp%10;
        temp=temp/10;
    }
    if(sum==temp2)
    {
        ret=0;
    }
    else {
    ret=1;
    }
    return ret;
}



int main()
{
    int t; 
    scanf("%d",&t);
    while(t--)
    {
        long n,i,j,res,max=0; 
        scanf("%ld",&n);
        for(i=100;i<1000;i++)
        {
            for(j=100;j<=999;j++)
            {
                res=i*j;
                if(pal(res)==0 && res>max && res<n)
                {
                    max=res;
                }
            }
        }
        printf("%ld\n",max);
    }
    return 0;
}
