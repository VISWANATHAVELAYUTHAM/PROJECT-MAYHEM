class Solution {
    public Node removeAllDuplicates(Node head) {
        // code here
        LinkedHashMap<Integer,Integer> hm = new LinkedHashMap<>();
        ArrayList<Node> list = new ArrayList<>();
        
        while(head != null)
        {
            hm.put(head.data,hm.getOrDefault(head.data,0)+1);
            head = head.next;
        }
        
        boolean isEnter = true;
        Node node = null;
        for(int item : hm.keySet())
        {
            if(hm.get(item) == 1)
            {
                list.add(new Node(item));
                int n = list.size();
                if(isEnter)
                {
                    node = list.get(0);
                    isEnter = false;
                }
                else
                {
                    node.next = list.get(n-1);
                    node = node.next;
                }
            }
        }
        
        head = list.get(0);
        
        return head;
    }
}
