class Solution {
    public int longestSubarray(int[] arr, int k) {
        // code here
        HashMap<Integer, Integer> prefixSumMap = new HashMap<>();
        int maxLength = 0;
        int prefixSum = 0;

        for (int i = 0; i < arr.length; i++) {
            prefixSum += arr[i];

            // Check if the prefix sum equals k
            if (prefixSum == k) {
                maxLength = i + 1;
            }

            // Check if there is a prefix sum such that removing it gives sum k
            if (prefixSumMap.containsKey(prefixSum - k)) {
                maxLength = Math.max(maxLength, i - prefixSumMap.get(prefixSum - k));
            }

            // Add the current prefix sum to the map if it is not already present
            if (!prefixSumMap.containsKey(prefixSum)) {
                prefixSumMap.put(prefixSum, i);
            }
        }

        return maxLength;
    }
}
