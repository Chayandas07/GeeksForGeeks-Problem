class Solution {
  public:
    long long countPairs(int n, int arr[], int k) {

        map<int,int> mp;

        for(int i=0;i<n;i++)

        {

            mp[arr[i]%k]++;

        }

        long long sum=0;

        for(auto v: mp){

        

            sum=sum+(v.second*(v.second-1))/2;

        }

        return sum;

    }
};
