Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@neelimadevi23 
AshokDon
/
Prefix_Sum-C-
1
00
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
Prefix_Sum-C-/3rd_subarray_sum_equal_to_zero.cpp
@AshokDon
AshokDon Rename subarray_sum_equal_to_zero.cpp to 3rd_subarray_sum_equal_to_ze…
…
Latest commit 1a3f176 yesterday
 History
 1 contributor
25 lines (23 sloc)  449 Bytes
  
//count the sub arrays whose sum is equal to zero or k
#include <iostream>
#include<bits/stdc++.h>
using namespace std;

int main() {
	int n=7,k=0;
	int arr[n]={4,-2,-1,1,-2,3,-3};
	map<int,int>dic;
	int count=0;
	dic.insert({0,1});
	int prefix=0;
	for(auto i:arr)
	{
	    prefix+=i;
	   
	    if(dic.find(prefix-k)!=dic.end())
	    {
	        count+=dic[prefix-k];
	    }
	    dic[prefix]+=1;
	}
	cout<<count;
	return 0;
}
