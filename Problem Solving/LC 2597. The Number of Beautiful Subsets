class Solution {
    private HashMap<Integer, Integer> freq;

    private int beautifulSubsets(int[] nums, int k, int i) {
        if (i == nums.length) { // base case
            return 1;
        }
        int result = beautifulSubsets(nums, k, i + 1); // nums[i] not taken
        if (!freq.containsKey(nums[i] - k) && !freq.containsKey(nums[i] + k)) { // check if we can take nums[i]
            freq.put(nums[i], freq.getOrDefault(nums[i], 0) + 1);
            result += beautifulSubsets(nums, k, i + 1); // nums[i] taken
            freq.put(nums[i], freq.get(nums[i]) - 1);
            if (freq.get(nums[i]) == 0) {
                freq.remove(nums[i]);
            }
        }
        return result;
    }

    public int beautifulSubsets(int[] nums, int k) {
        freq = new HashMap<Integer, Integer>();
        return beautifulSubsets(nums, k, 0) - 1; // -1 for empty subset
    }
}
