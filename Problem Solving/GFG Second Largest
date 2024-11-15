class Solution {
    public int getSecondLargest(int[] arr) {
        // Code Here
        HashSet<Integer> hm=new HashSet<>();
        for(int i:arr){
            hm.add(i);
        }
        if(hm.size()==1){
            return -1;
        }
        int k=0;
        int A[]=new int[hm.size()];
        for(int i:hm){
            A[k++]=i;
        }
        Arrays.sort(A);
        int n=A.length;
      
        return A[n-2];
    }
}
