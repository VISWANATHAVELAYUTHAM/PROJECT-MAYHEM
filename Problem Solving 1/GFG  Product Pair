class Solution {
    public boolean isProduct(int[] arr, long target) {
        Map<Long, Integer> mp = new HashMap<>();
        
        for(int val: arr) {
            long v = 1L * val;
            mp.put(v, mp.getOrDefault(v, 0) + 1);
        }
        
        for(int val: arr) {
            // Edge case
            if(val == 0) {
                if(target == 0) {
                    return true;
                }
                else {
                    continue;
                }
            }
            
            long v = 1L * val;
            long div = target / v;
            
            // Target is a square
            if(div == v) {
                if(mp.get(v) > 1 && v * v == target) {
                    return true;
                } 
            }
            // a * b
            else if(mp.containsKey(div)) {
                if(v * div == target) {
                    return true;
                } 
            }
        }
        
        return false;
    }
}
