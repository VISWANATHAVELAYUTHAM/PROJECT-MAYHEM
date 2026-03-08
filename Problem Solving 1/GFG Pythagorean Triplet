class Solution {
    boolean pythagoreanTriplet(int[] arr) {
        // code here
        boolean[] present = new boolean[1000001];
        for(int num : arr){
            present[num * num] = true;
        }
        for(int a = 1 ; a <= 1000 ; a++){
            if(!present[a * a]) continue;
            
            for(int b = a + 1 ; b <= 1000 ; b++){
                if(!present[b * b]) continue;
                
                int cSquare = a * a + b * b;
                if(cSquare > 1000000) continue;
                if(present[cSquare]){
                    return true;
                }
            }
        }
        return false;
        
    }
}
