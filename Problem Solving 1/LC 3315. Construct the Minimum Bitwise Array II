class Solution {
    public int[] minBitwiseArray(List<Integer> nums) {
        int[] ans = new int[nums.size()];

        for (int i = 0; i < nums.size(); i++) {
            int num = nums.get(i);

            if (num == 2) {
                ans[i] = -1;
                continue;
            }

            int numCopy = num;
            int count = 0;

            // Count consecutive 1s from the right
            while ((num & 1) == 1) {
                count++;
                num >>= 1;
            }

            // [count]th bit is the position of the last 1, like 100111 (count = 3)
            // Subtract the bit                                     ^
            ans[i] = numCopy - (1 << (count - 1));
        }

        return ans;
    }
}
