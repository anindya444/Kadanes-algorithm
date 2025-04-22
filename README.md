# Kadanes-algorithm
#include <iostream>
#include <vector>
using namespace std;
int maxsubarry(vector<int>&a)
{ int cs=0, ms=a[0];
    for(int i=0;i<a.size();i++)
    { cs=cs+a[i];
        if(cs<0)  //if current sum=cs is less than zero dont need to include it....assign it to zero.
        cs=0;
        if(ms<cs) // check for maximum;
        {ms=cs;}
    }
    return ms;}

int main()
{
  vector<int>a={2,14,-9,5,6};
  cout<< maxsubarry(a);
}
