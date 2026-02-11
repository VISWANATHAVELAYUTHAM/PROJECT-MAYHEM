class Solution {
    public int minCost(int[] heights, int[] cost) {
        // Step 1: Find the range of possible target heights
        int low = Integer.MAX_VALUE;
        int high = Integer.MIN_VALUE;

        for (int h : heights) {
            low = Math.min(low, h);     // Minimum height
            high = Math.max(high, h);   // Maximum height
        }

        int ans = Integer.MAX_VALUE;

        // Step 2: Use binary search to find the height that gives minimum cost
        while (low <= high) {
            int mid = (low + high) / 2;  // Try middle height

            // Calculate cost of converting all heights to mid, mid-1, and mid+1
            int costMid = helper(heights, cost, mid);
            int costLeft = helper(heights, cost, mid - 1);
            int costRight = helper(heights, cost, mid + 1);

            // Store the minimum cost
            ans = Math.min(ans, costMid);

            // Move the search towards the lower-cost direction
            if (costLeft < costMid) {
                high = mid - 1;
            } else if (costRight < costMid) {
                low = mid + 1;
            } else {
                break; // Found the best (local minimum) height
            }
        }

        return ans; // Return the minimum cost found
    }

    // Helper method to calculate cost of making all heights equal to target
    private int helper(int[] heights, int[] cost, int target) {
        int totalCost = 0;

        for (int i = 0; i < heights.length; i++) {
            // Cost = distance × cost[i]
            totalCost += Math.abs(heights[i] - target) * cost[i];
        }

        return totalCost;
    }
}
