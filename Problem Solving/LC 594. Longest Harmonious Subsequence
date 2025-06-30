class Solution {
    public int findLHS(int[] nums) {
       if(nums.length == 0){
           return 0;
       }
        Arrays.sort(nums);
        int left = 0, right = 1;
        int ArrayLen = 0;
        while(right < nums.length){
            int diff = nums[right]-nums[left];
            if(diff==1){
                ArrayLen = Math.max(ArrayLen, right-left+1);
            }
            if(diff <= 1){
                right++;
            }else{
                left++;
            }
        }
        return ArrayLen;
    }
}

//Time Complexity : O(nlogn), for sorting 
//Space Complexity : In worst case O(n), but in average case O(logn) space is required by sorting.
