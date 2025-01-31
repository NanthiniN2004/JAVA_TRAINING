##  QUEUE ARRAY IMPLEMENTATION

````java[]

class Queue{
    int front=-1;
    int rear=-1;
    int[] a=new int[8];
    public void enqueue(int data){
        if(rear>=a.length-1 ) {
        	System.out.println("Queue is full");
        }
        else {
        	if(front==-1) {
        		front=0;
        	}
        	rear++;
          a[rear]=data;
        }
    }
    public void dequeue(){
        if(front==-1 || front>rear) {
        	System.out.println("Queue is empty");
        }
        else {
          front++;
        }
    }
  
    public void display(){
           for(int i=front;i<=rear;i++) {
          System.out.println(" Display the elements "+a[i]);
        
    }
    }
    
}


public class Main {

	public static void main(String[] args) {
	Queue q=new Queue();
	q.enqueue(10);
	q.enqueue(20);
	q.enqueue(30);
	q.enqueue(40);
	q.enqueue(50);
	q.dequeue();
	q.display();
	}

}


output:

 Display the elements 20
 Display the elements 30
 Display the elements 40
 Display the elements 50

````
