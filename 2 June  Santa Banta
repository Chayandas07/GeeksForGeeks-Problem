class Solution{
public:
    vector<int>prime;
    void precompute(){
        // seive is done here...
        vector<bool>isprime(1e6+1,true);
        isprime[0]=false;
        isprime[1]=false;
        for(int i=2;i<1e6+1;i++)
        {
            if(isprime[i]==true)
            {
                prime.push_back(i);
                int j=2*i;
                while(j<1e6+1)
                {
                    isprime[j]=false;
                    j=j+i;
                }
            }
        }
    }
    void dfs(int node,vector<vector<int>>&adj,vector<int>&vis,int &teamsize){
        teamsize++; // value of teamsize is increased...
        vis[node]=1;
        for(auto child:adj[node]){
            if(vis[child]==0){
                dfs(child,adj,vis,teamsize);
            }
        }
    }
    int helpSanta(int n,int m,vector<vector<int>>&g){
        vector<int>vis(n+1,0);
        int maxi=0;
        for(int i=1;i<=n;i++){
            if(vis[i]==0){
                int teamsize=0; //initializing the teamsize variable...
                dfs(i,g,vis,teamsize); //dfs function to traverse through each connected nodes....
                maxi=max(maxi,teamsize); //maximizing the team size...
            }
        }
        if(maxi==1){
            return -1;
        }
        return prime[maxi-1];
    }
};
