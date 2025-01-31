## STACK OPERATION(PUSH,POP,PEEK) AND ARRAY IMPLEMENTATION

````java[]

package nandhu;

class Stack{
    int top=-1;
    int[] a=new int[8];
    public void push(int data){
        if(top==a.length-1) {
        	System.out.println("Stack is full");                  //push operation
        }
        else {
        	top++;
          a[top]=data;
        }
    }
    public void pop(){
        if(top==-1) {
        	System.out.println("Stack is empty");
        }                                                   //pop operation
        else {
          top--;
        }
    }
    public void peek(){
        if(top==-1) {
        	System.out.println("Stack is empty");
        }                                                   // peak Operation
        else {
          System.out.println(" top of the element"+a[top]);
        }
    }
    public void display(){
           for(int i=top;i>=0;i--) {
          System.out.println(" Display the elements "+a[i]);         //Display Method
        
    }
    }
    
}

public class Main {

	public static void main(String[] args) {
		Stack s=new Stack();
		s.push(10);
		s.push(20);
		s.push(30);
		s.push(40);
		s.push(50);
		s.pop();
		s.peek();
		s.display();
	}

}


OUTPUT:

top of the element40
 Display the elements 40
 Display the elements 30
 Display the elements 20
 Display the elements 10


````
