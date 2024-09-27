class Solution {
    // Function to find maximum of each subarray of size k.
    public ArrayList<Integer> max_of_subarrays(int k, int arr[]) {
        // Your code here
         ArrayList<Integer> list = new ArrayList<Integer>();
        
        int tempMax= findMax(0,k-1,arr);
        list.add(tempMax);
        
        for(int i=1; i<=arr.length-k; i++){
            if(tempMax == arr[i-1] ){
                tempMax = findMax(i, i+k-1,arr);
                list.add(tempMax);
            }
            else{
                    tempMax = Math.max(tempMax, arr[i+k-1]);
                    list.add(tempMax);
            }
        }
        return list;
        
    }
    
    public int findMax(int start, int end, int arr[]){
        int max=0;
        while(start <= end){
            max = Math.max(max, arr[start]);
            start++;
        }
        return max;
    }
}
