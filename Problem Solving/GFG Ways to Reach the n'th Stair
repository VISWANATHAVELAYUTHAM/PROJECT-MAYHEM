class Solution {
    int count(int n,int []dp){
        if(n==1||n==0)return 1;
        
        if(dp[n-1]!=-1)return dp[n-1];
        
        return dp[n-1]=count(n-1,dp)+count(n-2,dp);
    }
    int countWays(int n) {
        // your code here
        int []dp=new int [n];
    Arrays.fill(dp,-1);
    return count(n,dp);
    }
}
