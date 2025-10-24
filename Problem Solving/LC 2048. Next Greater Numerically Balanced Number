class Solution {
    long generate(long n, long current, long remaining, long[] count) {
        if (remaining == 0) {
            if (current > n) {
                for (int d = 1; d <= 9; d++) {
                    if (count[d] > 0 && count[d] != d) return 0;
                }
                return current;
            }
            return 0;
        }

        long result = 0;
        for (int d = 1; d <= 9 && result == 0; d++) {
            if (count[d] < d && d - count[d] <= remaining) {
                count[d]++;
                result = generate(n, current * 10 + d, remaining - 1, count);
                count[d]--;
            }
        }
        return result;
    }

    public int nextBeautifulNumber(int n) {
        String num = String.valueOf(n);
        long length = num.length();
        long[] count = new long[10];

        long result = generate(n, 0, length, count);
        java.util.Arrays.fill(count, 0);
        long nextLenResult = generate(0, 0, length + 1, count);
        if (result == 0) result = nextLenResult;
        return (int) result;
    }
}
