## 
````java[]

public class Main
{
	public static void main(String[] args) {
		for(int i=1;i<=10;i++){
		    if(i%2==0){
		        System.out.println("even number "+i);
		    }
		}
		for(int i=1;i<=10;i++){
		    if(i%2!=0){
		        System.out.println("odd number "+i);
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
	int fact=1;
		for(int i=1;i<=n;i++){
		    fact=fact*i;
		
		}
		System.out.println(fact);
	
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

		for(int i=1;i<=10;i++){
		   		System.out.println(i+"*"+n+"="+(i*n));
		
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
         int a=0;
         int b=1;
         System.out.println(a);
         System.out.println(b);
		for(int i=0;i<=n;i++){
		   	
		   	int c=a+b;
		   	a=b;
            b=c;
            
		 System.out.println(c);
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
	while(n!=0){
	    int a=n%10;
	    System.out.print(a);
	    n/=10;
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
   int count=0;
	while(n!=0){
	    int a=n%10;
	   
	    count++;
	    //System.out.print(a);
	    n/=10;
	}
	System.out.println("count of digit"+count);
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
    int sum=0;
	while(n!=0){
	    int a=n%10;
	   
	     if (a%2==0) {
	         sum=sum+a;
	     }
	    //System.out.print(a);
	    n/=10;
	}
	System.out.println("sum of the even digit "+sum);
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
   int a;
   int b=0;
   int temp=n;
    while(n!=0){
	     a=n%10;
	   // System.out.print(a);
	   b=b*10+a;
	    n/=10;
	    
	}
	System.out.println(b);
	if(temp==b){
	    System.out.println("palindrom");
	    
	}
	else{
	     System.out.println("not palindrom");
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
   int a;
  int temp=n;
  int sum=0;
    while(n!=0){
	     a=n%10;
	    int fact=1;
		for(int i=1;i<=a;i++){
		    fact=fact*i;
		}
		sum=sum+fact;

	    n/=10;
	    
	}
	System.out.println(sum);
	if(temp==sum){
	    System.out.println("Strong ");
	    
	}
	else{
	     System.out.println("not Strong");
	}
}
}

````

## 

````java[]

import java.util.*;
import java.lang.*;
public class Main
{
	public static void main(String[] args) {
   Scanner s=new Scanner(System.in);
   int n=s.nextInt();
   int temp=n;
   int t=n;
 
  int a;
  int count=0;
    while(n!=0){
	     a=n%10;
         count++;
	     n/=10;
	    
	}
	System.out.println(count);
	 double  sum=0;
	 double result;
	while(temp!=0){
	     a=temp%10;
         result=Math.pow(a,count);
	     temp/=10;
	    sum=sum+result;
	 
	}
        System.out.println(sum);
	
	if(t==sum){
	    System.out.println("Amstrong ");
	    
	}
	else{
	     System.out.println("not Amstrong");
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
     int sqr=n*n;
     while(n>0){
         if(n%10!=sqr%10){
             System.out.println("Not Automorphic number");
             break;
         }
         n/=10;
         sqr/=10;
     }
     if(n==0){
         System.out.println(" Automorphic number");
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
    for(int i=1;i<=10;i++){
        if(i==5){
            continue;
        }
        System.out.println(i);
    }
	}
}

````

## 

````java[]

import java.util.*;
import java.lang.*;

public class Main
{
	public static void main(String[] args) {
	    
   Scanner s=new Scanner(System.in);
   int n=s.nextInt();
   int temp=n;
   int re=n*n;
   System.out.println(re);
  int b=0;
   while(re!=0){
       int  a=re%10;
        b=b*10+a;
       re/=10;
   }
   System.out.println(b);
  int sqr=(int)Math.sqrt(b);
   System.out.println(sqr);
   int d=0;
   while(sqr!=0){
       int c=sqr%10;
        d=d*10+c;
       sqr/=10;
   }
    System.out.println(d);
    if(temp==d){
        System.out.println("adam number");
    }
    else{
        System.out.println("not adam number");
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
   int n1=s.nextInt();
   int n2=s.nextInt();
   int sum1=0;
   for(int i=1;i<n1;i++){
       if(n1%i==0){
           sum1+=i;
       }
   }
   int sum2=0;
   for(int i=1;i<n2;i++){
       if(n2%i==0){
           sum2+=i;
       }
   }
   int a=sum1/n1;
   int b=sum2/n2;
   if(a==b){
       System.out.println("Friendly pair");
   }
   else{
       System.out.println("not Friendly pair");
   }
	}
}

````

## 

````java[]

import java.util.*;
public class Main
{ 
    
    public int fact(int n){
        if(n==0){
            return 1;
        }
        return n*fact(n-1);
    }
    public double count(int n,int r){
        double res=fact(n)/fact(r)*fact(n-r);
        res=res/Math.pow(2,n);
        return res;
    }
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	  //  int p=s.nextInt();
	    int n=s.nextInt();
	    int r=s.nextInt();
        Main c=new Main();
     
    System.out.println( c.count(n,r));
     
}}

````

##
````java[]

import java.util.*;
public class Main
{ 
    	public static void main(String[] args) {


   int[][] arr=new int[10][10];
     Scanner s=new Scanner(System.in);
     for(int i=0;i<10;i++){
         for(int j=0;j<10;j++){
             arr[i][j]=s.nextInt();
         }
     }
     int sum=0;
     for(int i=0;i<10;i++){
         sum+=arr[i][i];
     }
     System.out.println(sum);
}}

````


