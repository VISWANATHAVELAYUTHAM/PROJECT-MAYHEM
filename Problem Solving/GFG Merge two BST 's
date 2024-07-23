class Solution {
    public List<Integer> merge(Node root1, Node root2) {
        List<Integer> list = new ArrayList<>();
        helper(root1, list);
        helper(root2, list);
        Collections.sort(list);
        return list;
    }
    void helper(Node root, List<Integer> list){
        if (root == null) return;
        list.add(root.data);
        helper(root.right, list);
        helper(root.left, list);
    }
}
