## Circular LinkedList(Insertion and Deletion)
````java[]

package circularlinkedlist;
import java.util.*;
class Node{
	int data;
	Node next;
	Node(int data)
	{
		this.data=data;
		this.next=null;
	}
}
class Circular{
	Node head;
	public Node insertatbegin(Node head,int data)
	{
		Node newnode=new Node(data);
		if(head==null)
		{
			newnode.next=newnode;
			head=newnode;
		}
		else {
			 Node temp=head;
			while(temp.next !=head)
			{
				temp=temp.next;
			}
				temp.next=newnode;
				newnode.next=head;
				head=newnode;
			}
		
		return head;
	}
	public Node insertatend(Node head,int data)
	{
		Node newnode=new Node(data);
		if(head==null)
		{
			newnode.next=newnode;
			head=newnode;
		}
		else {
			Node temp=head;
			while(temp.next!=head)
			{
				temp=temp.next;
			}
			temp.next=newnode;
			newnode.next=head;
		}
		return head;
	}
	public Node deleteatbegin(Node last)
	{
	
		if(head==null)
		{
			return null;
		}
		if(head==head.next)
		{
			head=null;
			return head;
		}
		Node cur=head;
		while(cur.next!=head)
		{
			cur=cur.next;
		}
		cur.next=head.next;
		head=head.next;
		return head;
	}
	public Node deleteatend(Node head)
	{
		if(head==null)
		{
			return null;
		}
		if(head==head.next)
		{
			head=null;
			return head;
		}
		Node cur=head;
		Node prev=null;
		while(cur.next!=head)
		{
			prev=cur;
			cur=cur.next;
		}
		prev.next=head;
		return head;
		
	}
	public void display(Node head)
	{
	
	if(head==null) {
		System.out.println("List empty");
		return;

	}
	else {
		Node temp=head;
		do{
			System.out.print(temp.data+" ");
			temp=temp.next;
		}while(temp!=head);
	}
	}
	
	
}
public class Main {

	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		Circular obj=new Circular();
		Node last=null;
		while(true)
		{
			int val=s.nextInt();
			if(val==-1)
			{
				break;
			}
			obj.head=obj.insertatend(obj.head,val);
		}
		System.out.println("After insert element");
		obj.display(obj.head);
		obj.deleteatbegin(obj.head);
		System.out.println("\nAfter delete the element");
		obj.display(obj.head);

	}

}

`````
