class Solution {
    boolean isSumTree(Node root) {
        // Your code here
        if(root == null || (root.left == null && root.right == null))
            return true;
        int ls = findSum(root.left);
        int rs = findSum(root.right);
        if(ls + rs == root.data){
            if(isSumTree(root.left) && isSumTree(root.right))
                return true;
        }
        return false;
    }
    
    int findSum(Node root){
        if(root == null)
            return 0;
        return root.data + findSum(root.left) + findSum(root.right);
    }
}
