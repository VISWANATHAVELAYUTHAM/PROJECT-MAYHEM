class Solution {
    public int kBitFlips(int[] arr, int k) {
        int n = arr.length;
        int[] isFlipped = new int[n];
        int flip = 0;
        int ans = 0;

        for (int i = 0; i < n; i++) {

            if (i >= k) {
                flip ^= isFlipped[i - k];
            }

            if ((arr[i] ^ flip) == 0) {
                if (i + k > n) {
                    return -1;
                }

                ans++;
                flip ^= 1;
                isFlipped[i] = 1;
            }
        }

        return ans;
    }
}
