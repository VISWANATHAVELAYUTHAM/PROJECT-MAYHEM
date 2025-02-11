class Solution {
    // Function to check whether a Binary Tree is BST or not.
    boolean isBST(Node root) {
        // code here.
        ArrayList<Integer>vt=new ArrayList<>();
        inorder(root,vt);
        for(int i=1;i<vt.size();i++)
        {
            if(vt.get(i-1)>vt.get(i))
            {
                return false;
            }
        }
        return true;
    }
    public static void inorder(Node root, ArrayList<Integer>vt)
    {
        if(root==null)
        return;
        inorder(root.left,vt);
        vt.add(root.data);
        inorder(root.right,vt);
    }
}
