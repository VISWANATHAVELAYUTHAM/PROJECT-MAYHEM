class Solution {
    int binarySearch(ArrayList<Integer> temp, int key){
        int index = 1;
        int low = 0;
        int high = temp.size()-1;
        while(low<=high){
            int mid = (low+high)/2;
            if(temp.get(mid) == key){
                index = mid;
                high = mid-1;
            }
            else if(temp.get(mid)>key){
                high = mid-1;
            }
            else{
                low = mid+1;
            }
        }
        return index;
    }
    int[] constructLowerArray(int[] arr) {
        // code here
        int[] res = new int[arr.length];
        ArrayList<Integer> temp = new ArrayList<>();
        for(int i = 0; i<arr.length; i++){
            temp.add(arr[i]);
        }
        Collections.sort(temp);
        for(int i=0; i<arr.length; i++){
            int index = binarySearch(temp, arr[i]);
            res[i] = index;
            temp.remove(index);
        }
        return res;
    }
}
