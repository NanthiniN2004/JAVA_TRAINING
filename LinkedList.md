## Check List is Empty or not
````java[]

class Node{
    int data;               
    Node next;
    Node(int data){
        this.data=data;
        this.next=null;
    }
}

class LinkedList{
    Node head,tail;
    public void insertAtEnd(int data){
        Node newnode=new Node(data);
       // newnode.next=head;
        if(head==null){
            System.out.println("List is empty");
            head=newnode;
            tail=newnode;
        }
        else{
            tail.next=newnode;
            tail=newnode;
        }
    }

    
    public void display()
    {
        Node temp=head;
        while(temp.next!=null){
            System.out.println(temp.data);
            temp=temp.next;
        }
    }
}

class Main{
    public static void main(String args[]){
        LinkedList link=new LinkedList();
        link.insertAtEnd(0);
     
    }
}

````

