class Solution {
    public int countIncreasing(int[] arr) {
       int n = arr.length;
        int totalCount = 0;
        int left = 0;

        for (int right = 1; right < n; right++) {
            // If the strictly increasing property breaks
            if (arr[right] <= arr[right - 1]) {
                left = right; // Move the left pointer to the start of a new segment
            }
            
            // If the window size is at least 2, 
            // the number of new subarrays ending at 'right' is (right - left)
            if (right > left) {
                totalCount += (right - left);
            }
        }

        return totalCount;
    }
}
