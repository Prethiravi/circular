  public class CreateList {  
    .  
    public class Node{  
        int data;  
        Node next;  
        public Node(int data) {  
            this.data = data;  
        }  
    }  
  
    public Node head = null;  
    public Node tail = null;  

    public void add(int data){  
         
        Node newNode = new Node(data);  

        if(head == null) {  
             //If list is empty, both head and tail would point to new node.  
            head = newNode;  
            tail = newNode;  
            newNode.next = head;  
        }  
        else {  
            .  
            tail.next = newNode;  
          
            tail = newNode;  
            //Since, it is circular linked list tail will point to head.  
            tail.next = head;  
        }  
    }  
  
    
    public void display() {  
        Node current = head;  
        if(head == null) {  
            System.out.println("List is empty");  
        }  
        else {  
            System.out.println("Nodes of the circular linked list: ");  
             do{  
                //Prints each node by incrementing pointer.  
                System.out.print(" "+ current.data);  
                current = current.next;  
            }while(current != head);  
            System.out.println();  
        }  
    }  
  
    public static void main(String[] args) {  
        CreateList cl = new CreateList();  
        
        cl.add(1);  
        cl.add(2);  
        cl.add(3);  
        cl.add(4);  
        //Displays all the nodes present in the list  
        cl.display();  



}
}
