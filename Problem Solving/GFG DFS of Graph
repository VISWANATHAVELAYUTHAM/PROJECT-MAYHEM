class Solution {
    void f(int ind,ArrayList<Integer> arr, ArrayList<ArrayList<Integer>> adj, boolean vis[]){
        vis[ind]=true;
        arr.add(ind);
        for(int it: adj.get(ind)){
            if(vis[it]==false){
                f(it, arr, adj, vis);
            }
        }
    }
    // Function to return a list containing the DFS traversal of the graph.
    public ArrayList<Integer> dfs(ArrayList<ArrayList<Integer>> adj) {
        boolean vis[]=new boolean[adj.size()]; 
        ArrayList<Integer> arr=new ArrayList<>();
        for(int i=0;i<adj.size();i++){
            if(vis[i]==false){
                f(i,arr, adj,vis);
            }
        }
        return arr;
        
    }
}
