class Solution {

    public ArrayList<Integer> Ancestors(Node root, int target) {
        ArrayList<Integer> ans = new ArrayList<>();
       
        dfs(root, ans, target);
        
        return ans;
        
    }
    public boolean dfs (Node root, ArrayList<Integer> ans, int target ){
        
        
        if(root == null) return false;
        
        if(root.data==target) return true;
        
        boolean left = dfs(root.left, ans, target);
        boolean right = dfs(root.right, ans, target);
        
        if(left||right){
            ans.add(root.data);
            return true;
        }
        
        return false;
        
        
       
       
        
        
    }
}
