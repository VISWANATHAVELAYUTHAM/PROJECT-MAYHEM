class Solution {
    public static int minimumCost(int n, int w, int[] cost) {
        // code here
         HashMap<String,Integer> hs=new HashMap<>();
        int a = solve(n,1,w,cost,hs);
        return (a==80000)?-1:a;
    }
    public static int solve(int n,int i,int w,int arr[],HashMap<String,Integer> hs){
        
        if(w==0)
            return 0;
        if(i-1==arr.length)
            return 80000;
        
        String key=i+"nik"+w;
        if(hs.containsKey(key))
            return hs.get(key);
            
        int a=80000,b=80000;
        if(w-i>=0 && arr[i-1]!=-1)
            a=arr[i-1]+solve(n,i,w-i,arr,hs);
        b=solve(n,i+1,w,arr,hs);
        
        int min = Math.min(a,b);
        hs.put(key,min);
        
        return min;
    }
}

