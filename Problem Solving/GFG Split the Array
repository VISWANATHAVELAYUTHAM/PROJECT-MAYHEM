class Solution {

    public static int countgroup(int arr[]) {
        // Complete the function
        int xor = 0;
        int n = arr.length;
        int mod = 1000000007;
        for(int i = 0; i<n; i++){
            xor ^= arr[i];
        }
        if(xor != 0) return 0;
        return (int)(Math.pow(2, n-1) - 1)%mod;
    }
}
