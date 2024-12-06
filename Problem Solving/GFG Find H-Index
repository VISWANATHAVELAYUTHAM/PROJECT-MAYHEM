class Solution {
    // Function to find hIndex
    public int hIndex(int[] citations) {
        // code here
        Arrays.sort(citations);
        int n = citations.length;
        int Hcount = 0;
        while(Hcount < n && citations[n-1-Hcount]>Hcount){
            Hcount++;
        }
        return Hcount;
    }
    
}
