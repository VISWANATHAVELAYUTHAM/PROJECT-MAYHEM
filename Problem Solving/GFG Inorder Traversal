class Solution {
    ArrayList<Integer>ans=new ArrayList<>();
    // Function to return a list containing the inorder traversal of the tree.
    ArrayList<Integer> inOrder(Node root) {
        // Code
          if(root==null)return ans;
        
      
            inOrder(root.left);
            ans.add(root.data);
            inOrder(root.right);
      
        
        return ans;
    }
}
