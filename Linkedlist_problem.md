## ROTATE THE LINKEDLIST 
````java[]


import java.util.*;

class Node
{
	int data;
	Node next;
	Node(int data)
	{
		this.data=data;
		this.next=null;
	}
}
class Linkedlist{
	Node head,tail;
	public void insertatbegin(int data)
	{
		Node newnode=new Node(data);
		if(head==null)
		{
			head=newnode;
		}
		else{
		    newnode.next=head;
		head=newnode;
		}
		
		
	}
	public void insertatend(int data)
	{
		Node newnode=new Node(data);
		if(head==null)
		{
			head=newnode;
			tail=newnode;
		}
		else{
		tail.next=newnode;
		tail=newnode;
		}
	}
	
	public Node rotate(Node head,int k)
	{
		Node curr=head;
		if(k==0 || curr==null)
		{
			return head;
		}
		int len=1;
	    while(curr.next !=null)
	    {
	    	curr=curr.next;        /// find the length of the linkedlist
	    	len++;
	    }
	    curr.next=head;          //make sll into circular linkedlist
	    k%=len;                  // maintain the k value
	    
	    curr=head;                // update curr pointer
	    for(int i=1;i<k;i++)
	    {
	    	curr=curr.next;        // move the curr pointer until reach k value
	    }
	    head=curr.next;           //split the link make new head 
	    curr.next=null;              
	    return head;
	}
	public void display() {
		Node temp=head;
		while(temp !=null)
		{
			System.out.print(temp.data+" ");
			temp=temp.next;
		}
	}

}
public class Main {

	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  Linkedlist obj=new Linkedlist();
	  while(true)
	  {
		  int val=s.nextInt();
		  if(val==-1)
		  {
			  break;
		  }
		  obj.insertatbegin(val);
	  }
	  obj.display();
	  System.out.println("\nEnter the k value");
	  int k=s.nextInt();
	  obj.head=obj.rotate(obj.head,k);
	  System.out.println("After rotate the linkedlist");
	  obj.display();

	}

}

OUTPUT:

50
40
30
20
10
-1
10 20 30 40 50 
Enter the k value
4
After rotate the linkedlist
50 10 20 30 40

`````

## FIND THE NTH NODE FROM THE LINKEDLIST
````JAVA[]


import java.util.*;

class Node
{
	int data;
	Node next;
	Node(int data)
	{
		this.data=data;
		this.next=null;
	}
}
class Linkedlist{
	Node head,tail;
	public void insertatbegin(int data)
	{
		Node newnode=new Node(data);
		if(head==null)
		{
			head=newnode;
		}
		else{
		    newnode.next=head;
		head=newnode;
		}
		
		
	}
	public void insertatend(int data)
	{
		Node newnode=new Node(data);
		if(head==null)
		{
			head=newnode;
			tail=newnode;
		}
		else{
		tail.next=newnode;
		tail=newnode;
		}
	}
	
	public int nthnode(Node head,int N) {
	    int len=0;
		Node temp=head;
		while(temp !=null)
		{
			len++;
			temp=temp.next;
		}
		if(len<N)
		{
		    return -1;
		}
		temp=head;
		for(int i=1;i<len-N+1;i++)
		{
		    temp=temp.next;
		}
		return temp.data;
	}

	public void display() {
		Node temp=head;
		while(temp !=null)
		{
			System.out.print(temp.data+" ");
			temp=temp.next;
		}
	}

}
public class Main {

	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  Linkedlist obj=new Linkedlist();
	  while(true)
	  {
		  int val=s.nextInt();
		  if(val==-1)
		  {
			  break;
		  }
		  obj.insertatbegin(val);
	  }
	  obj.display();
	  System.out.println("\nEnter the N value");
	  int N=s.nextInt();
	  System.out.println("Nth Node value "+ obj.nthnode(obj.head,N));
	

	}

}

output:

4
3
2
1
-1
1 2 3 4 
Enter the N value
3
Nth Node value 2

`````


