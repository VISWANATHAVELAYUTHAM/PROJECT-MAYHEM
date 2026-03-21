class Solution {
    public ArrayList<Integer> countBSTs(int[] arr) {
        
        int n = arr.length;
        long[] cat = getCatlan(n);
        
        int[] sorted = arr.clone();
        Arrays.sort(sorted);
        
        ArrayList<Integer> res = new ArrayList<Integer>();
        for(int i=0; i<n; i++) {
            int left = Arrays.binarySearch(sorted, arr[i]);
            int right = n -1 -left;
            res.add((int)(cat[left] * cat[right]));
        }
        return res;
    }
    
    private long[] getCatlan(int n) {
        
        long[] cat = new long[n+1];
        cat[0] = 1;
        
        if(n > 0) cat[1] = 1;
        for(int i=2; i<=n; i++) {
            for(int j=0; j<i; j++) {
                
                cat[i] += (cat[j] * cat[i -1 -j]);
            }
        }
        return cat;
    }
}
