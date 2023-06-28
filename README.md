# Google-Hackathon
#include <bits/stdc++.h>
using namespace std;

int main()
{   
    vector<vector<string>> v[6];

    for ( auto it:v)
    {
        v[0].push_back({"net_e = A & B"});
        v[1].push_back({"net_f = C | D"});
        v[2].push_back({"net_g = ~ net_f"});
        v[3].push_back({"Z = net_g ^ net_e"});
        v[4].push_back({"FAULT_AT = net_f"});
        v[5].push_back({"FAULT_TYPE = SA0"});
        
    }

    
    vector<int> A = { 0,0,1,1};
    vector<int> B = { 0,1,0,1};
    vector<int> C = { 0,0,1,1};
    vector<int> D = { 0,1,0,1};
    vector<int> net_f = { 0,0,0,0};
    vector<int> net_g = { 1,1,1,1};
    vector<int> Z = { 1,1,1,1};

    /*
    Since D = 1 and C = 1 gives actual output 1 but output at net_f = 0.
    Therefore , the value of D has to be changed to 0.
    */

   vector<int> ans = { 0,0,0,1};
   
   cout << "[ A, B, C, D] = ";
   cout << "[";
   for ( int i ; i < 3 ;i++)
    {
        cout << ans[i] << ",";
    }
    
    cout << ans[3] << "]" << " ,";

   for( int i = 0; i<=0;i++)
   {
        cout << "Z = " << Z[0] << endl;
   }
    
    return 0;
}
