class Solution {
    public static int kthSmallest(int[] arr, int k) {
        PriorityQueue<Integer> pq = new PriorityQueue<>(Collections.reverseOrder());
        for(int val : arr){
            pq.add(val);
            if(pq.size() > k) pq.poll();
        }
        return pq.poll();
    }
}
