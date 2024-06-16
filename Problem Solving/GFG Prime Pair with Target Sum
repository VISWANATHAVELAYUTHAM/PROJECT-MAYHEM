class Solution {
    public static boolean[] sieve(int n) {
        boolean[] isPrime = new boolean[n + 1];
        for (int i = 2; i <= n; i++) {
            isPrime[i] = true;
        }
        for (int p = 2; p * p <= n; p++) {
            if (isPrime[p]) {
                for (int i = p * p; i <= n; i += p) {
                    isPrime[i] = false;
                }
            }
        }
        return isPrime;
    }
    public static ArrayList<Integer> getPrimes(int n) {
         boolean[] isPrime = sieve(n);
        ArrayList<Integer> prime = new ArrayList<>();
        ArrayList<Integer> ans = new ArrayList<>();
        for(int i=2;i<=n;i++){
            if(isPrime[i]){
                prime.add(i);
            }
        }
        
        int i=0;
        int j=prime.size()-1;
        while(i<=j){
            int a = prime.get(i);
            int b = prime.get(j);
            if(a+b==n){
                ans.add(a);
                ans.add(b);
                return ans;
            }
            else if(a+b<n){
                i++;
            }
            else{
                j--;
            }
        }
        ans.add(-1);
        ans.add(-1);
        return ans;
    }
}

