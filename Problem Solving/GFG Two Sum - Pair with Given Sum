class Solution {
    boolean twoSum(int arr[], int target) {
        Map<Integer, Integer> map = new HashMap<>();
        
        for(int num : arr){
            map.put(num, map.getOrDefault(num, 0)+1);
        }
        
        for(int num : arr){
            int complement = target-num;
            
            if(map.containsKey(complement) && (complement != num || map.get(complement) > 1)){
                return true;
            }
        }
        
        return false;
    }
}
