class Solution{   
public:
     int cal(int i , int prev ,  int n , vector<vector<int>> &colors ,     vector<vector<int>>& dp)
     {
         if(i==n)
         return 0; 
         
         if(dp[i][prev+1]!=-1)
         return dp[i][prev+1] ;
         
         int take=0  , mini =INT_MAX;
         for(int j =0 ; j<3;j++)
         {
         if(prev==-1 || j!=prev)
         {
             take = colors[i][j] +cal(i+1 , j , n , colors , dp); 
         mini= min(mini , take ); 
         }
    
         }
         
         return dp[i][prev+1] = mini ;
     }


    int minCost(vector<vector<int>> &colors, int N) {
        // Write your code here.
        vector<vector<int>>dp(N+1, vector<int>(4, -1 )) ;
        return cal(0 , -1 ,N , colors , dp ) ;
    }
};
