class Solution{
public:
    bool makePalindrome(int n,vector<string> &arr){
        // Code here
        unordered_map<string,int> mp;
        
        for(auto i:arr)
        {
            mp[i]++;
        }
        
        int odd=0;
        for(auto i: mp)
        {
            string temp=i.first;
            reverse(temp.begin(),temp.end());
            
            if(i.first==temp)
            {
                if(i.second%2) // odd
                {
                    odd++;
                }
                if(odd>1)
                {
                    return false;
                }
            }
            else
            {
                if(i.second!=mp[temp])
                {
                    return false;
                }
            }
        }
        
        return true;
    }
};
