class Solution {
    int[] printKClosest(int[] arr, int k, int x) {
        // code here
        int[] result = new int[k];
        HashMap<Integer, Integer> map = new HashMap<>();
       for(int val : arr){
           if(x-val != 0){
           map.put(val,Math.abs(val - x));
           }
       }
      
        
       List<Map.Entry<Integer, Integer>> entryList = new ArrayList<>(map.entrySet());

        
        entryList.sort((a, b) -> {
            if (!a.getValue().equals(b.getValue())) {
                return a.getValue() - b.getValue();
            } else {
                return b.getKey() - a.getKey(); 
            }
        });

        for (int i = 0; i < k; i++) {
            result[i] = entryList.get(i).getKey();
        }

        return result;
    }
}
