class Solution {
    public static int[] productExceptSelf(int arr[]) {
        // code here
        int product=1;
        int count=0;
        for(int i:arr){
            if(i!=0) product*=i;
            else count++;
        }
        int ans[]=new int[arr.length];
        if(count>=2) return ans;
        for(int i=0;i<arr.length;i++){
            if(arr[i]!=0 && count==0) ans[i]=product/arr[i];
            else if(arr[i]!=0 && count>0) ans[i]=0;
            else ans[i]=product;
        }
        return ans;
    }
}
