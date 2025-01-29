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
##  LinkedList Insertion(Begin,End,Specific Position)

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
        if(head==null){            // Element add end position
            head=newnode;
            tail=newnode;
        }
        else{
            tail.next=newnode;
            tail=newnode;
        }
    }
    
  public void insertAtBegin(int data){
        Node newnode=new Node(data);
        newnode.next=head;                  //Element add Beginnig
        head=newnode;
    }
    
    public void display()
    {
        Node temp=head;
        while(temp!=null){                    //display list
            System.out.println(temp.data);
            temp=temp.next;
        }
    }
    
  public void specificPosition(int pos,int data){
        Node newnode=new Node(data);
        Node temp=head;                      //Insert at Specific Position
        for(int i=0;i<pos-1;i++){
            temp=temp.next;
}
            newnode.next=temp.next;
            temp.next=newnode;
    }
}

class Main{
    public static void main(String args[]){
        LinkedList link=new LinkedList();
        link.insertAtEnd(100);
         link.insertAtEnd(200);
         link.insertAtEnd(300);
           link.insertAtEnd(400);
          link.insertAtBegin(500);
          link.specificPosition(2,350);
           link.display();
    }
}


````
## LinkedList Deletion Operation(Beginning.Ending,Specific Position)

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
        if(head==null){            // Element add end position
            head=newnode;
            tail=newnode;
        }
        else{
            tail.next=newnode;
            tail=newnode;
        }
    }
    
  public void insertAtBegin(int data){
        Node newnode=new Node(data);
        newnode.next=head;                  //Element add Beginnig
        head=newnode;
    }
    
    public void display()
    {
        Node temp=head;
        while(temp!=null){                    //display list
            System.out.println(temp.data);
            temp=temp.next;
        }
    }
    
  public void specificPosition(int pos,int data){
        Node newnode=new Node(data);
        Node temp=head;                      //Insert at Specific Position
        for(int i=0;i<pos-1;i++){
            temp=temp.next;
        } 
            newnode.next=temp.next;
            temp.next=newnode;
            
    }
    public void deleteAtBegin(){
        if(head !=null){                // Delete at Element Beginnig
        head=head.next;
      }
    }
    public void deleteAtEnd(){
        Node temp=head;
        while(temp.next.next!=null){        // Delete at End position
            temp=temp.next;
        }
        temp.next=null;
    }
 public void DeleteSpecificPosition(int pos){
        Node temp=head;                      
        for(int i=0;i<pos;i++){
            temp=temp.next;                      // Delete at speicifc Position
        } 
            head.next=temp.next;
        
            
    }
}

class Main{
    public static void main(String args[]){
        LinkedList link=new LinkedList();
        link.insertAtEnd(100);
         link.insertAtEnd(200);
         link.insertAtEnd(300);
           link.insertAtEnd(400);
          link.insertAtBegin(500);
         link.insertAtBegin(600);
          link.specificPosition(3,350);
          link.deleteAtBegin();
          link.deleteAtEnd();
        link.DeleteSpecificPosition(3);
           link.display();
    }
}
