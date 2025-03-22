class Solution {
    int stealing(int ind, int arr[], int dp[], int start) {
        if (ind < start) return 0;

        if (dp[ind] != -1) return dp[ind];

        int notsteal = stealing(ind - 1, arr, dp, start);
        int steal = arr[ind] + stealing(ind - 2, arr, dp, start);

        return dp[ind] = Math.max(notsteal, steal);
    }

    int maxValue(int[] arr) {
        int n = arr.length;
        if (n == 1) return arr[0]; // Only one house, just take it

        int[] dp1 = new int[n];
        int[] dp2 = new int[n];
        Arrays.fill(dp1, -1);
        Arrays.fill(dp2, -1);

        // Case 1: Exclude last house
        int case1 = stealing(n - 2, arr, dp1, 0);
        // Case 2: Exclude first house
        int case2 = stealing(n - 1, arr, dp2, 1);

        return Math.max(case1, case2);
    }
}
