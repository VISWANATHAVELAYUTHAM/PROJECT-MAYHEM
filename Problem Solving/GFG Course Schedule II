class Solution {
    public ArrayList<Integer> findOrder(int n, int[][] prerequisites) {
        // code here
        @SuppressWarnings("unchecked")
        ArrayList<Integer>[] graph = (ArrayList<Integer>[]) new ArrayList[n];
        Queue<Integer> q = new LinkedList<>();
        ArrayList<Integer> ans = new ArrayList<>();
        int[] indeg = new int[n];
        
        for(int i = 0; i < n; i++) graph[i] = new ArrayList<>();
        
        for(int i = 0; i < prerequisites.length; i++){
            graph[prerequisites[i][1]].add(prerequisites[i][0]);
            indeg[prerequisites[i][0]]++;
        }
        
        for(int i = 0; i < n; i++){
            if(indeg[i] == 0){
                q.add(i);
                ans.add(i);
            }
        }
        
        while(!q.isEmpty()){
            for(int neigh : graph[q.remove()]){
                indeg[neigh]--;
                if(indeg[neigh] == 0){
                    q.add(neigh);
                    ans.add(neigh);
                }
            }
        }
        
        return ans;
    }
}
