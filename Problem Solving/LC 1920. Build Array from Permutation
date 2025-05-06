class Solution {

    //using recursion
    public int[] buildArray(int[] nums) {
        aPermutation(nums,0);

        return nums;
    }
    
    void aPermutation(int[] nums,int start){
        if(start<nums.length){
        int temp=nums[start];
        int result=nums[temp];
        aPermutation(nums,start+1);
        nums[start]=result;
    }
  
    }
}
