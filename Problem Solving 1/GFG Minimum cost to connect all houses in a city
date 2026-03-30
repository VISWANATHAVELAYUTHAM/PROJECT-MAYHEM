class Solution {

    public int minCost(int[][] houses) {
        // code here
        int n=houses.length;
        PriorityQueue<int[]> pq=new PriorityQueue<>((a,b)->a[1]-b[1]);
        boolean[] visited=new boolean[n];
        
        pq.add(new int[]{0,0});
        
        int minCost=0;
        int edges=0;
        
        while(edges<n && !pq.isEmpty()){
            int[] temp=pq.poll();
            int node=temp[0];
            int cost=temp[1];
            
            if(visited[node]) continue;
            visited[node]=true;
            
            minCost+=cost;
            
            for(int i=0; i<n; i++){
                int dist=Math.abs(houses[i][0]-houses[node][0])+Math.abs(houses[i][1]-houses[node][1]);
                pq.add(new int[]{i,dist});
            }
            
            edges++;
        }
        
        return minCost;
    }
}
