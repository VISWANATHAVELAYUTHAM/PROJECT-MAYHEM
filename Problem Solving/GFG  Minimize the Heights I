class Solution {
    public int getMinDiff(int k, int[] arr) {
        
        // code here
        Arrays.sort(arr);
        
        int n = arr.length;
        int res = arr[n-1] - arr[0];
        
        for(int i =1;i<n;i++){
            int max = Math.max(arr[n-1]-k,arr[i-1]+k);
            int min = Math.min(arr[0]+k, arr[i]-k);
            
                res = Math.min(res,max-min);
        }
        
        return res;
    }
}
