class Solution {
    static int rec(int i,int wt[],int val[],int w){
        if(i<0) return 0;
        int p=0,np=0;
        if(w-wt[i]>=0) p=val[i]+rec(i-1,wt,val,w-wt[i]);
        np=rec(i-1,wt,val,w);
        return Math.max(p,np);
    }
    // Function to return max value that can be put in knapsack of capacity W.
    static int knapSack(int W, int wt[], int val[]) {
        // your code here
        int n=wt.length;
        return rec(n-1,wt,val,W);
    }
}
