class Solution {
    public int countPaths(int n, int[][] roads) {
        // code here
        long MOD = 1_000_000_007L;
        List<List<long[]>> adj = new ArrayList<>();
        for(int i=0; i<n; i++)
            adj.add(new ArrayList<>());
            
        for(int[] road : roads)
        {
            adj.get(road[0]).add(new long[]{road[1], road[2]});
            adj.get(road[1]).add(new long[]{road[0], road[2]});
        }
        
        long[] dist = new long[n];
        long[] ways = new long[n];
        Arrays.fill(dist, Long.MAX_VALUE);
        
        dist[0] = 0;
        ways[0] = 1;
        
        PriorityQueue<long[]> pq = new PriorityQueue<>
        (Comparator.comparingLong(a -> a[0]));
        
        pq.add(new long[]{0,0});
        
        while(!pq.isEmpty())
        {
            long[] top = pq.poll();
            long d = top[0];
            int u = (int) top[1];
            
            if(d>dist[u])   continue;
            
            for(long[] neighbor : adj.get(u)) {
                int v = (int) neighbor[0];
                long weight = neighbor[1];
                
                if(dist[u] + weight < dist[v])  {
                    dist[v] = dist[u] + weight;
                    ways[v] = ways[u];
                    pq.add(new long[]{dist[v] , v});
                }
                
                else if(dist[u] + weight == dist[v])    {
                    ways[v] = (ways[v] + ways[u]) %MOD;
                }
            }
        }
        
        return (int) ways[n-1];
    }
}
