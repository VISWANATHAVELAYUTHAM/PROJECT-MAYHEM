class Solution {
    public ArrayList<ArrayList<Integer>> combinationSum(int n, int k) 
    {
        ArrayList<ArrayList<Integer>> ans = new ArrayList<>();
        ArrayList<Integer> sb = new ArrayList<>();
        int sum =0;
        solve(n,k,ans,sb,0,1);
        return ans;
    }
    
    public void solve(int n, int k,ArrayList<ArrayList<Integer>> ans, ArrayList<Integer> sb ,int sum,int start )
    {
        if(sb.size() == k)
        {
            if(n == sum)
            {
            ans.add(new ArrayList<>(sb));
            return;
        }
        return;
        }
        for(int i =start;i<=9;i++)
        {
            sum += i;
            sb.add(i);
            solve(n,k,ans,sb,sum,i+1);
            sum -= i;
            sb.remove(sb.size()-1);
            
        }
    }
}

