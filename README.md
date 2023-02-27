
class Solution
{
    //Function to remove a loop in the linked list.
    public static void removeLoop(Node head){
        // code here
        // remove the loop without losing any nodes
        HashSet<Node>set=new HashSet<>();
        Node prev=null;
        Node curr=head;
        while(curr!=null)
        {
            if(set.contains(curr))
            {
                prev.next=null;
                return;
            }
            set.add(curr);
            prev=curr;
            curr=curr.next;
            
        }
    }
}
