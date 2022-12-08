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
  ![image](https://user-images.githubusercontent.com/117881871/206474207-f3f25139-422d-4e58-96fc-c4b5aa6c1d7e.png)  
