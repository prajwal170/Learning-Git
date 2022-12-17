#include<bits/stdc++.h>

using namespace std;

vector<vector<string>> final_ans;

void solve(vector<pair<string,float>> arr,int i,float sum,vector<string> ans,int limit){

    if(i == arr.size()){
        if(ans.size() > 1)
        final_ans.push_back(ans);
        return ;
    }

    if(sum + arr[i].second <= limit){
        ans.push_back(arr[i].first);
        solve(arr,i+1,sum+arr[i].second,ans,limit);
        ans.pop_back();
    }
    solve(arr,i+1,sum,ans,limit);

}


int main(){

    vector<vector<float>> vect(5,vector<float>(7,0));
    float sum=0.0;

    unordered_map<int,string> m;
    vector<pair<string,float>> arr;
    m[0] = "TOI";
    m[1] = "Hindu";
    m[2] = "ET";
    m[3] = "BM";
    m[4] = "HT";

    float limit;
    cin>>limit;
     for(int i=0;i<5;i++){
        sum=0.0;
        for(int j=0;j<7;j++){
            float x=0.0;
            cin>>x;
            vect[i][j] = x;
            sum+=vect[i][j];
        }


        arr.push_back({m[i],sum});
        
    }

  
   

    cout<<limit<<endl;



    solve(arr,0,0.0,{},limit);
  

    for(int i=0;i<final_ans.size();i++){
        cout<<"{";
        for(int j=0;j<final_ans[i].size();j++){
            if(j==final_ans[i].size()-1)
            cout<<final_ans[i][j];
            else
            cout<<final_ans[i][j]<<",";
        }
        cout<<"}";
    }

    cout<<endl;

    
    return 0;
}
