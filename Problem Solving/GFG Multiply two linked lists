class Solution {
    public long multiplyTwoLists(Node first, Node second) {
        // Code here
        Node temp1 = first;
        Node temp2 = second;
        long sum1 = 0, sum2 = 0;
        long mod = (long)1e9+7;
        
        while(temp1 != null)
        {
            sum1 = sum1*10 + temp1.data;
            temp1 = temp1.next;
        }
        while(temp2 != null)
        {
            sum2 = sum2*10 + temp2.data;
            temp2 = temp2.next;
        }
        
        //System.out.println(sum1 +" "+ sum2);
        
        return (sum1 * sum2)%mod;
    }
}
