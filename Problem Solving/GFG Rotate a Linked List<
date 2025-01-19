class Solution {
    public Node rotate(Node head, int k) {
        // add code here
        int size=0;
        Node head1=head;
        Node prev=null;
        while(head1!=null){
            prev=head1;
            head1=head1.next;
            size++;
        }
        k=k%size;
        while(k-->0){
            Node temp=head.next;
            prev.next=head;
            prev=prev.next;
            head.next=null;
            head=temp;
            
        }
        return head;
    }
}
