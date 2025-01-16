class Solution {
    public int maxLen(int[] arr) {
        
        /*Replacing 0 with -1 will make this problem same as 
        finding the length of the longest subarray whose sum is 0*/
        
        Map<Integer,Integer> mp=new HashMap<>();
        mp.put(0,0);
        
        int res=0;
        int currSum=0;
        
        for(int i=0;i<arr.length;i++){
            
            currSum+=(arr[i]==0)?-1:1;
            
            if(currSum==0){
                res=i+1;
            }
            else if(mp.containsKey(currSum)){
                 res=Math.max(res,i-mp.get(currSum));
            }
            
            if(!mp.containsKey(currSum)){
                mp.put(currSum,i);
            }
            
        }
        
        return res;
    }
}
