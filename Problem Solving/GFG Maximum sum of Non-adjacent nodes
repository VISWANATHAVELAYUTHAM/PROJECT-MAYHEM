class Solution {
    static HashMap<String, Integer> dp;
    
    public int getMaxSum(Node root) {
        dp = new HashMap<>();
        return solver(root, false);
    }

    static int solver(Node root, boolean take) {
        if (root == null)
            return 0;
        
        String key = root.hashCode() + "_" + take; // Unique key for (node, take)
        if (dp.containsKey(key))
            return dp.get(key);
        
        int c = 0;
        if (take == false) {
            c = root.data + solver(root.left, true) + solver(root.right, true);
        }
        
        int max = solver(root.left, false) + solver(root.right, false);
        
        int ans = Math.max(max, c);
        dp.put(key, ans);
        return ans;
    }
}
