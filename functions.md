## EXAMPLE FUNCTION PROGRAM

````JAVA[]

import java.util.*;
public class Main
{
   static int add(int a,int b){
        int c=a+b;
        return c;
    }
static  int sub(int a,int b){
        return a-b;
    }
static  int mul(int a,int b){
        return a*b;
    }
    static void display(){
        Scanner s=new Scanner(System.in);
       int a=s.nextInt();
       int  b=s.nextInt();
       	System.out.println(add(a,b));
        System.out.println(sub(a,b));
        System.out.println(mul(a,b));
    }
    
    
    
	public static void main(String[] args) {
	    
	display();
	}
}

````
