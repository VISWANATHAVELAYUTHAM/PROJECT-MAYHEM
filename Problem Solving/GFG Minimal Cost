class Solution {
    public int minimizeCost(int k, int arr[]) {
        int[] dp = new int[arr.length];
        Arrays.fill(dp,100000);
        dp[0] = 0;   // cost for first stone
        
        for(int i=0 ; i<arr.length-1 ; i++) {
            for(int j=i+1;j<arr.length && j<=i+k ; j++) {
                
                // Explore next k stones
                
                dp[j] = Math.min(dp[j], dp[i] + Math.abs(arr[i]-arr[j]));
            }
        }
        
        return dp[arr.length-1];
    }
}
