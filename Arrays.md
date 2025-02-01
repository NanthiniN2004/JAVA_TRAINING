## Find Minimum and Maximum

````java[]

public class Main
{
	public static void main(String[] args) {
	    int a[]={1,11,22,3,2,5,6,10,8};
	 int  max=a[0];
	 int min=a[0];
		for(int i=1;i<a.length;i++){
	
		    if(max<a[i]){
		        max=a[i];
		    }
		    if(min>a[i]){
		        min=a[i];
		    }
		   
		}
		System.out.println(max);
	   System.out.println(min);
	}
	
	}
````


## Element found or not

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	   Scanner s=new Scanner(System.in);
	    int n=s.nextInt();
	  int a[]=new int[n];
	  boolean found=false;

	  int target=s.nextInt();
	  for(int i=0;i<n;i++){
	      a[i]=s.nextInt();
	  }
	  for(int i=0;i<n;i++){
	      if(a[i]==target){
	      	         found=true;
	      }
	      
	  }
	 System.out.println(found);
	
	}
}

````


## Sort the given array

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	   Scanner s=new Scanner(System.in);
	    int n=s.nextInt();
	    int a[]=new int[n];

	  for(int i=0;i<n;i++){
	      a[i]=s.nextInt();
	  }
	  for(int i=0;i<n;i++){
	     for(int j=0;j<n;j++){
	         if(a[i]<a[j]){
	    int temp=a[i];
	    a[i]=a[j];
	    a[j]=temp;
	         }
	  }
	  }
	  System.out.println("After sorting");
	  for(int i=0;i<n;i++){
	       System.out.println(a[i]);
	  }

	
	}
}

````


## Find the second largest Element

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	   Scanner s=new Scanner(System.in);
	    int n=s.nextInt();
	    int a[]=new int[n];

	  for(int i=0;i<n;i++){
	      a[i]=s.nextInt();
	  }
	  for(int i=0;i<n;i++){
	     for(int j=0;j<n;j++){
	         if(a[i]<a[j]){
	    int temp=a[i];
	    a[i]=a[j];
	    a[j]=temp;
	         }
	  }
	  }
	  System.out.println("Second largest element");
	
          System.out.println(a[n-2]);
	
	}
}

````


## Remove the duplicate element

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	   Scanner s=new Scanner(System.in);
	    int n=s.nextInt();
	    int a[]=new int[n];

	  for(int i=0;i<n;i++){
	      a[i]=s.nextInt();
	  }
	  Arrays.sort(a);
	  for(int i=0;i<n;i++){

	   if(i==0 || a[i]!=a[i-1]){
	      
	      System.out.println(a[i]);
	   }
	
	  }
	
	}
}

````


## Print the duplicate Element

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	   Scanner s=new Scanner(System.in);
	    int n=s.nextInt();
	    int a[]=new int[n];

	  for(int i=0;i<n;i++){
	      a[i]=s.nextInt();
	  }

          Arrays.sort(a);
	  for(int i=0;i<n-1;i++){
	   if(a[i]==a[i+1]){
	 	  System.out.println("duplicate element"+a[i]);
	       
	   }
	  
	  }

	
	}
}

````


## Merge the two array

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	   Scanner s=new Scanner(System.in);
	    int n=s.nextInt();
	    int a[]=new int[n];
	    int b[]=new int[n];
	    int c[]=new int[n+n];
        
     System.out.println("Enter the first array");
	  for(int i=0;i<n;i++){
	      a[i]=s.nextInt();
	  }
	  System.out.println("Enter the second array");
	  for(int i=0;i<n;i++){
	      b[i]=s.nextInt();
	  }

	  for(int i=0;i<n;i++){
     c[i]=a[i];
	   }
	   for(int i=0;i<n;i++){
	       c[n+i]=b[i];
	   }
	    System.out.println("" + Arrays.toString(c));

	
	}
}
````


## PASCAL TRIANGLE

````java[]
import java.util.*;
public class Main{
    public static void main(String args[]){
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=1;i<=n;i++){
            int val=1;
            for(int j=1;j<=i;j++){
                System.out.print(val+" ");
                val=val*(i-j)/j;
            }
            System.out.println();
        }
    }
}
OUTPUT


5
1 
1 1 
1 2 1 
1 3 3 1 
1 4 6 4 1 


