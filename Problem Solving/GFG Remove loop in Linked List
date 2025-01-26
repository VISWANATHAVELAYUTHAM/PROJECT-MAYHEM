class Solution {
    // Function to remove a loop in the linked list.
    public static void removeLoop(Node head) {
        // code here
        if(head==null)
        return;
         HashSet<Node> s = new HashSet<Node>();
         s.add(head);
        while(head!=null){
            if(s.contains(head.next)){
                head.next=null;
                return;
            }
            else
            s.add(head.next);
            head= head.next;
        }
    }
}
