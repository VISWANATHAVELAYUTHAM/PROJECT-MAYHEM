class Solution {
    public List<int[]> mergeOverlap(int[][] arr) {
        // Code here // Code here
        PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> a[0] - b[0]);
        for (int[] interval : arr) {
            pq.offer(interval);
        }
        
        List<int[]> ans = new ArrayList<>();
        int[] current = pq.poll();
        while (!pq.isEmpty()) {
            int[] next = pq.poll();
            if (current[1] >= next[0]) {
                current[1] = Math.max(current[1], next[1]);
            } else {
                ans.add(current);
                current = next;
            }
        }
        ans.add(current);
        return ans;
    }
}
