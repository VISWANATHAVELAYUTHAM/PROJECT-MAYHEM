class Solution {
    List<Integer> leftBoundary = new ArrayList<>();
    List<Integer> rightBoundary = new ArrayList<>();
    List<Integer> leafNodes = new ArrayList<>();
    ArrayList<Integer> boundaryTraversal(Node node) {
        // code here
        leftBoundary.add(node.data);
        populateLeftBoundary(node.left);
        populateRightBoundary(node.right);
        ArrayList<Integer> result = new ArrayList<>();
        result.addAll(leftBoundary);
        result.addAll(leafNodes);
        result.addAll(rightBoundary);
        return result;
    }
    
    void populateLeftBoundary(Node node) {
        if (node == null) {
            return;
        }
        if (node.left == null && node.right == null) {
            leafNodes.add(node.data);
            return;
        }
        leftBoundary.add(node.data);
        if (node.left != null) {
            populateLeftBoundary(node.left);
            populateLeafNodes(node.right);
        } else {
            populateLeftBoundary(node.right);
        }
    }
    
    void populateLeafNodes(Node node) {
        if (node == null) {
            return;
        }
        if (node.left == null && node.right == null) {
            leafNodes.add(node.data);
            return;
        }
        populateLeafNodes(node.left);
        populateLeafNodes(node.right);
    }
    
    void populateRightBoundary(Node node) {
        if (node == null) {
            return;
        }
        if (node.left == null && node.right == null) {
            leafNodes.add(node.data);
            return;
        }
        if (node.right != null) {
            populateLeafNodes(node.left);
            populateRightBoundary(node.right);
        } else {
            populateRightBoundary(node.left);
        }
        rightBoundary.add(node.data);
    }
}
