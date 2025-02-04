class Solution {
    // Helper class to store height and diameter together
     public static class Func {
        int height;
        int diameter;
        Func(int height, int diameter) {
            this.height = height;
            this.diameter = diameter;
        }
    }
    public static Func diameterFind(Node root) {
        if (root == null) return new Func(0, 0);
        Func left = diameterFind(root.left);
        Func right = diameterFind(root.right);
        int height = Math.max(left.height, right.height) + 1;
        int diameter = Math.max(left.height + right.height, Math.max(left.diameter, right.diameter));
        return new Func(height, diameter);
    }
    public static int diameter(Node root) {
        //CODE HERE
        return diameterFind(root).diameter;
    }
}
