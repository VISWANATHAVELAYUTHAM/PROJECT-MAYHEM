class Solution {
    public Node cloneLinkedList(Node head) {
        // code here
        if(head==null) return head;
        Node t = head;
        while(t!=null){
            Node n = t.next;
            Node x = new Node(t.data);
            t.next=x;
            x.next=n;
            t=n;
        }
        t = head;
        while(t!=null){
            Node n = t.next;
            if(t.random!=null){
                n.random=t.random.next;
            }
            t=n.next;
        }
        t=head;
        Node newHead = t.next,p=newHead;
        
        while(t!=null){
            Node a = p.next;
            t.next=a;
            t=a;
            if(a!=null) p.next=a.next;
            p=p.next;
        }
        
        return newHead;
    }
}

