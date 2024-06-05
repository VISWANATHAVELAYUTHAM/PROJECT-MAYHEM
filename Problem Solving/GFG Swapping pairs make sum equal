class Solution {
    long findSwapValues(long a[], int n, long b[], int m) {
        long sumA = 0, sumB = 0;
        
        for (long num : a) {
            sumA += num;
        }
        for (long num : b) {
            sumB += num;
        }
        
        long diff = sumA - sumB;
        
        // If diff is odd, return -1 since we can't split the difference evenly
        if (diff % 2 != 0) {
            return -1;
        }
        
        // We are looking for x - y = diff / 2
        long targetDiff = diff / 2;
        
        HashSet<Long> setB = new HashSet<>();
        for (long num : b) {
            setB.add(num);
        }
        
        for (long x : a) {
            long y = x - targetDiff;
            if (setB.contains(y)) {
                return 1;
            }
        }
        
        return -1;
    }
}
