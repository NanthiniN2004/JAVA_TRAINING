## Hollow Square
````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
	
		for(int i=1;i<=n;i++){
		    for(int j=1;j<=n;j++){
		        if(i==1 || i==n || j==1|| j==n){
		             System.out.print("* ");
		        }
		        else{     
		            System.out.print("  ");
		    }
		    }
		    System.out.println();
		}
	}
}


output:

5
* * * * * 
*       * 
*       * 
*       * 
* * * * *

````
## Square
````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		for(int i=1;i<=n;i++){
		    for(int j=1;j<=n;j++){
		    
		             System.out.print("* ");
		    }
		    System.out.println();
		}
	}
}


output:
5
* * * * * 
* * * * * 
* * * * * 
* * * * * 
* * * * * 
````

## Right Angle Triangle
````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		for(int i=1;i<=n;i++){
		    for(int j=1;j<=i;j++){
		    
		             System.out.print("* ");
		    }
		    System.out.println();
		}
	}
}
output:

5
* 
* * 
* * * 
* * * * 
* * * * *

````
## Rectamgle
````java[]

 import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		int m=s.nextInt();
		for(int i=1;i<=n;i++){
		    for(int j=1;j<=m;j++){
		    
		             System.out.print("* ");
		    }
		    System.out.println();
		}
	}
}

output:

5
4
* * * * 
* * * * 
* * * * 
* * * * 
* * * * 

````
## Parallelogram
````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		for(int i=1;i<=n;i++){
		     for(int k=1;k<=n-i;k++){
		            System.out.print(" ");
		        }
		    for(int j=1;j<=n;j++){
		    
		            System.out.print("* ");
		    }
		    System.out.println();
		}
	}
}

output:
5
    * * * * * 
   * * * * * 
  * * * * * 
 * * * * * 
* * * * * 
````
## Mirror Right Angle Triangle
````java[]


import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		for(int i=1;i<=n;i++){
		     for(int k=1;k<=n-i;k++){
		            System.out.print("  ");
		        }
		    for(int j=1;j<=i;j++){
		    
		            System.out.print(" *");
		    }
		    System.out.println();
		}
	}
}


output

5
         *
       * *
     * * *
   * * * *
 * * * * *
````
## 
