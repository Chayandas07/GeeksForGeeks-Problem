class Solution{
public:
  void merging(vector<long long> &pre, int l, int m, int h, long long &inv) {
        int i = l, j = m + 1, k = 0;
        vector<long long> temp(h - l + 1);
    
        while(i <= m and j <= h) {
            if(pre[i] <= pre[j])
                temp[k++] = pre[i++];
            else {
                inv += (m - i + 1);
                temp[k++] = pre[j++];
            }
        }
        
        while(i <= m) temp[k++] = pre[i++];
        
        while(j <= h) temp[k++] = pre[j++];
        
        k = 0;
        for(int c = l; c <= h; c++)
            pre[c] = temp[k++];
    }

    void mergeSort(vector<long long> &pre, int l, int h, long long &inv) {
        if(l < h) {
            int mid = (l + h) >> 1;
            mergeSort(pre, l, mid, inv);
            mergeSort(pre, mid + 1, h, inv);
            merging(pre, l, mid, h, inv);
        }
    }
    
    long long inversions(vector<long long> &pre) {
        int n = pre.size();
        long long inv = 0;
        
        mergeSort(pre, 0, n - 1, inv);
        
        return inv;
    }
    
    long long countSubstring(string s){
        int n = s.size();
        
        vector<int> nums(n); 
        for(int i = 0; i < n; i++) {
            nums[i] = s[i] - '0';
            if(nums[i] == 0)
                nums[i] = -1;
        }
        
        vector<long long> pre_sum(n);
        long long sum = 0;
        for(int i = 0; i < n; i++) {
            sum += nums[i];
            pre_sum[i] = sum;
        }
        
        long long count = 0; // to store valid substrings;
        for(int i = 0; i < n; i++) {
            if(pre_sum[i] > 0) count++;
        }
        
        reverse(pre_sum.begin(), pre_sum.end());
        
        return count + inversions(pre_sum);
    }
};
