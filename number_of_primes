
#include<bits/stdc++.h>
using namespace std;
int main()
  { 
signed int n=1000;
signed int sieve[1000]={0};

    
    sieve[0]=1;
    sieve[1]=1;
    for(signed int i=2;i*i<=n;i++)
    {
        if(sieve[i]==0)
        {
            
          for(signed int j=i*i;j<=n;j+=i)
          {
            sieve[j]=1;
          }
        }
    }


    signed int num;
    cin>>num;
    
    for(signed int i=2;i<=num;i++)
    {
    if(sieve[i]==0)
        cout<<i<<" ";
    }
    
  return 0;    
}

