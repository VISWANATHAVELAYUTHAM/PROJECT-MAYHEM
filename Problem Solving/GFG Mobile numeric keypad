class Solution {
    
    // Keypad layout
    private static final int[][] keyPad = {
        {1, 2, 3}, 
        {4, 5, 6}, 
        {7, 8, 9}, 
        {-1, 0, -1}
    };
    
    // Possible movements: right, left, down, up
    private static final int[] dirX = {0, 0, 1, -1};
    private static final int[] dirY = {1, -1, 0, 0};
    
    public long getCount(int N) {
        // Edge case: If N is 1, return 10 (all single digits)
        if (N == 1) return 10;
        
        // dpPrevious stores the number of sequences of length l-1 ending at each key
        long[] dpPrevious = new long[10];
        long[] dpCurrent = new long[10];
        
        // Initialize dpPrevious for sequences of length 1
        for (int i = 0; i < 10; i++) {
            dpPrevious[i] = 1;
        }
        
        // Build dp table iteratively
        for (int length = 2; length <= N; length++) {
            for (int i = 0; i < 4; i++) {
                for (int j = 0; j < 3; j++) {
                    if (keyPad[i][j] != -1) {
                        int key = keyPad[i][j];
                        dpCurrent[key] = dpPrevious[key];
                        
                        // Check all possible moves
                        for (int k = 0; k < 4; k++) {
                            int newI = i + dirX[k];
                            int newJ = j + dirY[k];
                            
                            if (newI >= 0 && newJ >= 0 && newI < 4 && newJ < 3 && keyPad[newI][newJ] != -1) {
                                dpCurrent[key] += dpPrevious[keyPad[newI][newJ]];
                            }
                        }
                    }
                }
            }
            // Swap dpCurrent and dpPrevious for the next iteration
            long[] temp = dpPrevious;
            dpPrevious = dpCurrent;
            dpCurrent = temp;
        }
        
        // Sum up the results for sequences of length N
        long ans = 0;
        for (int i = 0; i < 10; i++) {
            ans += dpPrevious[i];
        }
        
        return ans;
    }
}
