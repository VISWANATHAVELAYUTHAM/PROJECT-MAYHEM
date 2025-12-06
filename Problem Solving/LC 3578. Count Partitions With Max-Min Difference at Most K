import java.util.*;

class Solution {
    static final long MOD = 1_000_000_007;

    public int countPartitions(int[] nums, int k) {
        int n = nums.length;

        long[] dp = new long[n + 1];
        long[] prefix = new long[n + 1];

        dp[0] = 1;           
        prefix[0] = 1;

        Deque<Integer> minQ = new ArrayDeque<>();
        Deque<Integer> maxQ = new ArrayDeque<>();

        int l = 0;

        for (int r = 0; r < n; r++) {

            while (!minQ.isEmpty() && nums[minQ.peekLast()] > nums[r])
                minQ.pollLast();
            minQ.addLast(r);

            while (!maxQ.isEmpty() && nums[maxQ.peekLast()] < nums[r])
                maxQ.pollLast();
            maxQ.addLast(r);

            while (!minQ.isEmpty() && !maxQ.isEmpty()
                    && nums[maxQ.peekFirst()] - nums[minQ.peekFirst()] > k) {

                if (minQ.peekFirst() == l) minQ.pollFirst();
                if (maxQ.peekFirst() == l) maxQ.pollFirst();
                l++;
            }

            long ways = prefix[r] - (l == 0 ? 0 : prefix[l - 1]);
            ways = (ways % MOD + MOD) % MOD;

            dp[r + 1] = ways;
            prefix[r + 1] = (prefix[r] + dp[r + 1]) % MOD;
        }

        return (int) dp[n];
    }
}
