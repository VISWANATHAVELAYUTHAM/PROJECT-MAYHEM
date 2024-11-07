class Solution {

    public List<Integer> findSplit(int[] arr) {
        
        // Return an array of possible answer, driver code will judge and return true or
        // false based on
        
        
        List<Integer> list = new ArrayList<>();
        int total = Arrays.stream(arr).sum();
        
        if(total%3!=0){
            list.add(-1);
            list.add(-1);
            return list;
        }
        
        int s =0;
        int result = total/3;
        
        for(int i =0;i<arr.length;i++){
            s+=arr[i];
            if(s==result){
                s=0;
                list.add(i);
            }
            if(list.size()==2){
                return list;
            }
        }
        
        list.add(-1);
        list.add(-1);
        return list;
    }
}
