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
##  Singly LinkedList Insertion(Begin,End,Specific Position)

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
##  Singly LinkedList Deletion Operation(Beginning.Ending,Specific Position)

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


````

## DOUBLY LINKED LIST(INSERT AT BEGIN,INSERT AT END)

````java[]

class Node{
    int data;
    Node next;
    Node prev;
    Node(int data){
        this.data=data;
        this.next=null;
        this.prev=null;
    }
}
class DLL{
    Node head,tail;
    public void insertAtBegin(int data)
    {
        Node newnode=new Node(data);
        if(head==null){                           //Insert the element in Beginning
            head=newnode;
            tail=newnode;
        }
        else{
            newnode.next=head;
            head.prev=newnode;
            head=newnode;
            
        }
    }
    public void insertAtEnd(int data){
        Node newnode=new Node(data);
        if(tail==null)
        {
            head=tail=newnode;                     /// Insert the element in End position
            
        }
        else{
            tail.next=newnode;
            newnode.prev=tail;
            tail=newnode;
            
        }
    }
   
    public void display(){
        Node temp=head;
    if(temp==null){
        System.out.println("List is Empty");
    }
    else{
        while(temp!=null){
            System.out.print(temp.data+"<-->");
            temp=temp.next;
        }
        System.out.println();
    }
        
    }
    
} 
public class Main{
    public static void main(String args[]){
        DLL obj=new DLL();
        obj.insertAtBegin(100);
       obj.insertAtBegin(200);
       obj.insertAtBegin(300);
       obj.insertAtEnd(500);
       obj.insertAtEnd(400);
       obj.display();
    }
}

output:

300<-->200<-->100<-->500<-->400


## DOUBLY LINKED LIST (DELETION AT BEGIN,DELETION AT END)

````java[]

class Node{
    int data;
    Node next;
    Node prev;
    Node(int data){
        this.data=data;
        this.next=null;
        this.prev=null;
    }
}
class DLL{
    Node head,tail;
    public void insertAtBegin(int data)
    {
        Node newnode=new Node(data);
        if(head==null){                           //Insert the element  in Beginning
            head=newnode;
            tail=newnode;
        }
        else{
            newnode.next=head;
            head.prev=newnode;
            head=newnode;
            
        }
    }
    public void insertAtEnd(int data){
        Node newnode=new Node(data);
        if(tail==null)
        {
            head=tail=newnode;                     /// Insert the element in End position
            
        }
        else{
            tail.next=newnode;
            newnode.prev=tail;
            tail=newnode;
            
        }
    }
    public void deleteAtBegin(){
        if(head==null)
        {
            System.out.println("List is Empty");
        }
        if(head==tail){
            head=tail=null;                       //Delete the  Element in Beginning
        }
        else{
            head=head.next;
            head.prev=null;
        }
    }
    
    public void deleteAtEnd(){
        if(head==null)
        {
            System.out.println("List is Empty");
        }
        if(head==tail){                                   // Delete the element in End position
            head=tail=null;
        }
        else{
            tail=tail.prev;
            tail.next=null;
        }
    }
    public void display(){
        Node temp=head;
    if(temp==null){
        System.out.println("List is Empty");
    }
    else{
        while(temp!=null){
            System.out.print(temp.data+"<-->");
            temp=temp.next;
        }
        System.out.println();
    }
        
    }
    
} 
public class Main{
    public static void main(String args[]){
        DLL obj=new DLL();
        obj.insertAtBegin(100);
       obj.insertAtBegin(200);
       obj.insertAtBegin(300);
       obj.insertAtEnd(500);
       obj.insertAtEnd(400);
   obj.deleteAtBegin();
       obj.deleteAtEnd();
       obj.display();
    }
}


OUTPUT:

200<-->100<-->500<

````
