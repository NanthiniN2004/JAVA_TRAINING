## Program 1
````java[]

import java.util.*;

public class Person
{  
   String name;
   int age;
   
   Person(String n,int a){
       this.name=n;
       this.age=a;
   }
    
  void display(){
      System.out.println("name " +name);
       System.out.println("age  " +age);
  }
   
	public static void main(String[] args) {
	Person p= new Person("Nanthu",20);
	p.display();


	}
}

````

## Program 2

````java[]

import java.util.*;

public class Rectangle
{  
   int  length;
   int breadth;

   
   Rectangle(int l,int b){
       this.length=l;
       this.breadth=b;
      
   }
    
  void area(){
      int ar=length*breadth;
      System.out.println("Area " +ar);
   
  }
  void Perimeter(){
      int pe=2*(length+breadth);
      System.out.println("Perimeter " +pe);
   
  }
   
	public static void main(String[] args) {
	 Scanner s=new Scanner(System.in);
	 int length=s.nextInt();
	 int breadth=s.nextInt();
	Rectangle r=new Rectangle(length,breadth);
	r.area();
	r.Perimeter();


	}
}

````

## Program 3

````java[]

import java.util.*;
 class check{
     int n;
     void evenorodd(int n){
         if(n%2==0){
             System.out.println("even");
         }
         else{
             System.out.println("odd");
         }
     }
 }
public class Main
{  
	public static void main(String[] args) {
     check c=new check();
     c.evenorodd(10);
}}

````

## Program 4

````java[]

import java.util.*;
 class check{
     int p;
     int n;
     int r;
     int  simple(int p,int n,int r){
        return (p*n*r)/100;
     }
 }
public class Main
{  
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	    int p=s.nextInt();
	    int n=s.nextInt();
	    int r=s.nextInt();
     check c=new check();
    System.out.println(c.simple(p,n,r));
     
}}


````
