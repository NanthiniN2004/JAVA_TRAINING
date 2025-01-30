##
````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	     char ch=s.next().charAt(0);
	     if((ch>='a'&& ch<='z')||( ch>='A' && ch<='Z')){
	         if((ch=='a' ||ch=='e' || ch=='i' ||ch=='o'||ch=='u') || (ch=='A' ||ch=='E' || ch=='I' ||ch=='O'||ch=='U')){
	             System.out.println("vowels");
	             
	         }
	     }
	     else{
	         if(ch>='0' && ch<='9'){
	             System.out.println("numbers");
	         }
	         else{
	             System.out.println("symbol");
	         }
	     }
		}
	}

````


## 

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	    int a=s.nextInt();
	    int b=s.nextInt();
		System.out.println("Enter the symbol");
		char c=s.next().charAt(0);
		switch(c){
		    case '+':
		        System.out.println(a+b);
		        break;
		     case '-':
		         System.out.println(a-b); 
		        break;
		        
		    case '*':
		         System.out.println(a*b); 
		        break;
		    case '/':
		         System.out.println(a/b); 
		        break;
		     default:
		     System.out.println("no");   
		}
	}
}

````

## 

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	     int n=s.nextInt();
	     if(n%4 ==0 || (n%400==0 && (n%100 !=0))){
	         System.out.println( "ít is leap year" );
	     
	     }
	     else{
	         System.out.println("not leap year");
	     }
	    
		}
	}

````

## 

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	    float x=s.nextFloat();
	    float y=s.nextFloat();
	    if((x>(12*y)))
	    {
	        System.out.println("loss");
	        float loss=x-(12*y);
	        System.out.println("loss value"+ loss);
	    }
	    else{
	        System.out.println("profit");
	    }
	}
}

````
