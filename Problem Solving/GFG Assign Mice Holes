class Solution {
    public int assignHole(int[] mices, int[] holes) {
        // code here
       
        Arrays.sort(mices);
        Arrays.sort(holes);

        int n = mices.length;
        int maxTime = 0;

       
        for (int i = 0; i < n; i++) {
            maxTime = Math.max(maxTime, Math.abs(mices[i] - holes[i]));
        }

        return maxTime;
    }
};
