class Solution {
  public:
    vector<long long> nextLargerElement(vector<long long> &arr, int n){
        // Your code here
        vector<long long> ans(n);
        stack<long long> s;
        ans[n-1] = -1;
        s.push(arr[n-1]);
        for(int i=n-2;i>=0;i--){
            if(!s.empty()){
                if(s.top() <= arr[i]){
                    s.pop();
                    i++;
                }
                else{
                    ans[i] = s.top();
                    s.push(arr[i]);
                }
            }
            else{
                ans[i] = -1;
                s.push(arr[i]);
            }
        }
        return ans;
    }
};
