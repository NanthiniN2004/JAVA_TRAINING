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

## SORT 0s,1s and 2s in Linked list
````java[]

package sll;
import java.util.*;

class Node {
	int data;
	Node next;
	Node(int data) {
		this.data = data;
		this.next = null;
	}
}

class Sll {
	Node head, tail;

	public void insertatbegin(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			newnode.next = head;
			head = newnode;
		}
	}

	public void insertatend(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			tail.next = newnode;
			tail = newnode;
		}
	}

	public void display() {
		Node cur = head;
		while (cur != null) {
			System.out.print(cur.data + " ");
			cur = cur.next;
		}
	}

	public Node sortlist(Node head) {
		if (head == null || head.next == null) {
			return head;
		}

		Node zeron = new Node(0);
		Node onen = new Node(0);
		Node twon = new Node(0);
		Node zero = zeron, one = onen, two = twon;

		Node temp = head;
		while (temp != null) {
			if (temp.data == 0) {
				zero.next = temp;
				zero = zero.next;
			} else if (temp.data == 1) {
				one.next = temp;
				one = one.next;
			} else {
				two.next = temp;
				two = two.next;
			}
			temp = temp.next;
		}
		zero.next = (onen.next != null) ? onen.next : twon.next;
		one.next = twon.next;
		two.next = null;

		return zeron.next;
	}
}

public class Main {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Sll obj = new Sll();

		while (true) {
			int val = s.nextInt();
			if (val == -1) break;
			obj.insertatend(val); 
		}

		System.out.println("\nAfter insert the element");
		obj.display();

		obj.head = obj.sortlist(obj.head);

		System.out.println("\nAfter sort the element");
		obj.display();
	}
}


OUTPUT:

1
2
1
1
0
2
-1

After insert the element
1 2 1 1 0 2 
After sort the element
0 1 1 1 2 2

`````

## Merge a linked list into another linked list at alternate positions

````java[]

package sll;
import java.util.*;

class Node {
	int data;
	Node next;
	Node(int data) {
		this.data = data;
		this.next = null;
	}
}

class Sll {
	Node head, tail;

	public void insertatbegin(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			newnode.next = head;
			head = newnode;
		}
	}

	public void insertatend(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			tail.next = newnode;
			tail = newnode;
		}
	}

	public void display(Node head) {
		Node cur = head;
		while (cur != null) {
			System.out.print(cur.data + " ");
			cur = cur.next;
		}
	}

	public List<Node> merge(Node head1,Node head2)
	{
		Node temp1=head1;
		Node temp2=head2;
		
		while(temp1!=null && temp2!=null)
		{
			Node ptr1=temp1.next;
			Node ptr2=temp2.next;
			temp2.next=temp1.next;
			temp1.next=temp2;
			temp1=ptr1;
			temp2=ptr2;
			
					
		}
		return Arrays.asList(head1, temp2);
		
	}
}

public class Main {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Sll obj = new Sll();
        System.out.println("Enter the element list1");
		while (true) {
			int val = s.nextInt();
			if (val == -1) break;
			obj.insertatend(val); 
		}
		Sll obj1 = new Sll();
		System.out.println("Enter the element list2");
		while (true) {
			int val1 = s.nextInt();
			if (val1 == -1) break;
			obj1.insertatend(val1); 
		}

		System.out.println("\nAfter insert the element list 1");
		obj.display(obj.head);
		System.out.println("\nAfter insert the element list 2");
		obj1.display(obj1.head);
       System.out.println("\nAfter merge the element");
	   List<Node> res=obj.merge(obj.head,obj1.head);
	   obj.display(res.get(0));
       obj.display(res.get(1));
	}
}


OUTPUT:

Enter the element list1
1
2
3
-1
Enter the element list2
4
5
6
7
8
-1

After insert the element list 1
1 2 3 
After insert the element list 2
4 5 6 7 8 
After merge the element
1 4 2 5 3 6 7 8

`````
## Merge two sorted linked lists
````java[]

package sll;
import java.util.*;

class Node {
	int data;
	Node next;
	Node(int data) {
		this.data = data;
		this.next = null;
	}
}

class Sll {
	Node head, tail;

	public void insertatbegin(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			newnode.next = head;
			head = newnode;
		}
	}

	public void insertatend(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			tail.next = newnode;
			tail = newnode;
		}
	}

	public void display(Node head) {
		Node cur = head;
		while (cur != null) {
			System.out.print(cur.data + " ");
			cur = cur.next;
		}
	}

	public Node mergeSorted(Node head1,Node head2)
	{
		Node dummy=new Node(0);
		Node temp=dummy;
		while(head1 !=null && head2 !=null)
		{
			if(head1.data<head2.data)
			{
				temp.next=head1;
				head1=head1.next;
			}
			else {
				temp.next=head2;
				head2=head2.next;
			}
			temp=temp.next;
		}
		if(head1 !=null)
		{
			temp.next=head1;
		}
		else {
			temp.next=head2;
		}
		return dummy.next;
	}
	public List<Node> mergealterposition(Node head1,Node head2)
	{
		Node temp1=head1;
		Node temp2=head2;
		
		while(temp1!=null && temp2!=null)
		{
			Node ptr1=temp1.next;
			Node ptr2=temp2.next;
			temp2.next=temp1.next;
			temp1.next=temp2;
			temp1=ptr1;
			temp2=ptr2;
			
					
		}
		return Arrays.asList(head1, temp2);
		
	}
}

public class Main {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Sll obj = new Sll();
        System.out.println("Enter the element list1");
		while (true) {
			int val = s.nextInt();
			if (val == -1) break;
			obj.insertatend(val); 
		}
		Sll obj1 = new Sll();
		System.out.println("Enter the element list2");
		while (true) {
			int val1 = s.nextInt();
			if (val1 == -1) break;
			obj1.insertatend(val1); 
		}

		System.out.println("\nAfter insert the element list 1");
		obj.display(obj.head);
		System.out.println("\nAfter insert the element list 2");
		obj1.display(obj1.head);
       System.out.println("\nAfter merge the element");
	    obj.mergeSorted(obj.head,obj1.head);
	    obj.display(obj.head);
	}
}


OUTPUT:

Enter the element list1
5
10
15
40
-1
Enter the element list2
2
3
20
-1

After insert the element list 1
5 10 15 40 
After insert the element list 2
2 3 20 
After merge the element
5 10 15 20 40

````

## Delete last occurrence of an item from linked list
````java[]

package sll;
import java.util.*;

class Node {
	int data;
	Node next;
	Node(int data) {
		this.data = data;
		this.next = null;
	}
}

class Sll {
	Node head, tail;

	public void insertatbegin(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			newnode.next = head;
			head = newnode;
		}
	}

	public void insertatend(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			tail.next = newnode;
			tail = newnode;
		}
	}

	public void display(Node head) {
		Node cur = head;
		while (cur != null) {
			System.out.print(cur.data + " ");
			cur = cur.next;
		}
	}
	public Node deleteatbegin(Node head)
	{
		if(head !=null)
		{
		Node temp=head;
		head=head.next;
		temp=null;
		}
		return head;
	}
	
	public Node deleteatend(Node head)
	{
		if(head==null)
		{
			return null;
		}
		if(head.next==null)
		{
			return null;
		}
		Node temp=head;
		while(temp.next.next !=null)
		{
			temp=temp.next;
		}
		temp.next=null;
		return head;
	}
public Node lastoccurence(Node head,int key)
{
	Node last=null,lastprev=null,prev=null;
	Node curr=head;
	while(curr!=null)
	{
		if(curr.data==key)
		{
			lastprev=prev;
			last=curr;
		}
		prev=curr;
		curr=curr.next;
	}
	if(last !=null)
	{
		if(lastprev !=null)
		{
			lastprev.next=last.next;
		}
		else {
			head=head.next;
		}
	}
	return head;
}
	public Node deleteatspecific(Node head,int pos)
	{
		Node temp=head;
		Node prev=null;
		if(temp==null)
		{
			return head;
		}
		if(pos==1)
		{
			head=temp.next;
			return head;
		}
		for(int i=1;temp!=null && i<pos;i++)
		{
			prev=temp;
			temp=temp.next;
		}
		if(temp!=null)
		{
			prev.next=temp.next;
		}
		else {
			System.out.println("Element not found");
		}
		return head;
		
	}
	
	
}

public class Main {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Sll obj = new Sll();
        System.out.println("Enter the element list1");
		while (true) {
			int val = s.nextInt();
			if (val == -1) break;
			obj.insertatend(val); 
		}

		System.out.println("\nAfter insert the element list 1");
		obj.display(obj.head);
		System.out.println("\nEnter the key value");
		int pos=s.nextInt();
		System.out.println("After delete the last occurence  element");
		obj.lastoccurence(obj.head,pos);
		
	    obj.display(obj.head);
	}
}

OUTPUT:

Enter the element list1
1
2
3
1
2
4
-1

After insert the element list 1
1 2 3 1 2 4 
Enter the key value
2
After delete the last occurence  element
1 2 3 1 4

`````
    
  ##   Remove Duplicates from a Sorted Linked List 

  ````java[]
package sll;
import java.util.*;

class Node {
	int data;
	Node next;
	Node(int data) {
		this.data = data;
		this.next = null;
	}
}

class Sll {
	Node head, tail;

	public void insertatbegin(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			newnode.next = head;
			head = newnode;
		}
	}

	public void insertatend(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			tail.next = newnode;
			tail = newnode;
		}
	}

	public void display(Node head) {
		Node cur = head;
		while (cur != null) {
			System.out.print(cur.data + " ");
			cur = cur.next;
		}
	}
	public Node deleteatbegin(Node head)
	{
		if(head !=null)
		{
		Node temp=head;
		head=head.next;
		temp=null;
		}
		return head;
	}
	
	public Node deleteatend(Node head)
	{
		if(head==null)
		{
			return null;
		}
		if(head.next==null)
		{
			return null;
		}
		Node temp=head;
		while(temp.next.next !=null)
		{
			temp=temp.next;
		}
		temp.next=null;
		return head;
	}
public Node lastoccurence(Node head,int key)
{
	Node last=null,lastprev=null,prev=null;
	Node curr=head;
	while(curr!=null)
	{
		if(curr.data==key)
		{
			lastprev=prev;
			last=curr;
		}
		prev=curr;
		curr=curr.next;
	}
	if(last !=null)
	{
		if(lastprev !=null)
		{
			lastprev.next=last.next;
		}
		else {
			head=head.next;
		}
	}
	return head;
}
	public Node deleteatspecific(Node head,int pos)
	{
		Node temp=head;
		Node prev=null;
		if(temp==null)
		{
			return head;
		}
		if(pos==1)
		{
			head=temp.next;
			return head;
		}
		for(int i=1;temp!=null && i<pos;i++)
		{
			prev=temp;
			temp=temp.next;
		}
		if(temp!=null)
		{
			prev.next=temp.next;
		}
		else {
			System.out.println("Element not found");
		}
		return head;
		
	}
	

	public Node removeduplicate(Node head)
	{
		Node temp=head;
		while(temp!=null && temp.next!=null)
		{
			if(temp.data==temp.next.data)
			{
				temp.next=temp.next.next;
			}
			else {
				temp=temp.next;
			}
		}
		return head;
	}
}

public class Main {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Sll obj = new Sll();
        System.out.println("Enter the element list1");
		while (true) {
			int val = s.nextInt();
			if (val == -1) break;
			obj.insertatend(val); 
		}
		Sll obj1 = new Sll();
		System.out.println("\nAfter insert the element list 1");
		obj.display(obj.head);
		System.out.println("\nAfter delete the deplicate elements");
		obj.removeduplicate(obj.head);
		
	    obj.display(obj.head);
	}
}


OUTPUT:
Enter the element list1
1
2
2
3
3
3
4
-1

After insert the element list 1
1 2 2 3 3 3 4 
After delete the deplicate elements
1 2 3 4

````

## Pairwise Swap Elements of a given Linked List

````java[]

package sll;
import java.util.*;

class Node {
	int data;
	Node next;
	Node(int data) {
		this.data = data;
		this.next = null;
	}
}

class Sll {
	Node head, tail;

	public void insertatbegin(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			newnode.next = head;
			head = newnode;
		}
	}

	public void insertatend(int data) {
		Node newnode = new Node(data);
		if (head == null) {
			head = tail = newnode;
		} else {
			tail.next = newnode;
			tail = newnode;
		}
	}

	public void display(Node head) {
		Node cur = head;
		while (cur != null) {
			System.out.print(cur.data + " ");
			cur = cur.next;
		}
	}		
	public void deletewithouthead(Node pos)
	{
		if(pos==null)
		{
			return;
		}
		else {
			if(pos.next==null)
			{
				System.out.println("Empty");
				return;
			}
		}
		pos.data=pos.next.data;
		pos.next=pos.next.next;
	}
	public Node pairwiseswap(Node head)
	{
		Node temp=head;
		while(temp!=null && temp.next!=null)
		{
			int cur=temp.data;
			temp.data=temp.next.data;
			temp.next.data=cur;
		    temp=temp.next.next;
		}
		return head;
	}
}

public class Main {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Sll obj = new Sll();
        System.out.println("Enter the element list1");
		while (true) {
			int val = s.nextInt();
			if (val == -1) break;
			obj.insertatend(val); 
		}
		Sll obj1 = new Sll();
		System.out.println("\nAfter swap the element ");
	    obj.display(obj.head);
	}
}

OUTPUT:
Enter the element list1
1
2
3
4
5
6
-1

After insert the element list 1
1 2 3 4 5 6 
After swap the element 
2 1 4 3 6 5 
`````
