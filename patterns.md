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
		    for(int j=1;j<=i;j++){
		    
		            System.out.print(" *");
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

## 

````java[]

 import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		for(int i=n;i>=1;i--){
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

output:

5
 * * * * *
   * * * *
     * * *
       * *
         *
````

## 

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		for(int i=n;i>=1;i--){
		     for(int k=1;k<=n-i;k++){
		            System.out.print(" ");
		        }
		    for(int j=1;j<=i;j++){
		    
		            System.out.print(" *");
		    }
		    System.out.println();
		}
	}
}

output:

5
 * * * * *
  * * * *
   * * *
    * *
     *

````

## 

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

		for(int i=n-1;i>=1;i--){
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


output:
5
         *
       * *
     * * *
   * * * *
 * * * * *
   * * * *
     * * *
       * *
         *

````

## 

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		
	for(int i=1;i<=n-1;i++){
		    for(int j=1;j<=i;j++){
		    
		             System.out.print(" *");
		    }
		    System.out.println();
		}


		for(int i=n;i>=1;i--){
		    
		    for(int j=1;j<=i;j++){
		    
		            System.out.print(" *");
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
 * * * *
 * * *
 * *
 *

````

## 

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
		    for(int j=1;j<=i;j++){
		    
		            System.out.print(" *");
		    }
		    System.out.println();
		}
           for(int i=n-1;i>=1;i--){
		     for(int k=1;k<=n-i;k++){
		            System.out.print(" ");
		        }
		    for(int j=1;j<=i;j++){
		    
		            System.out.print(" *");
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
  * * * *
   * * *
    * *
     *

````

## 

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
		    for(int j=1;j<=(2*i)-1;j++){
		    
		            System.out.print(" *");
		    }
		    System.out.println();
		}
          

	

		
	}
}

output:

5
         *
       * * *
     * * * * *
   * * * * * * *
 * * * * * * * * *


````

## 

````java[]

import java.util.Scanner;

public class Main {
    public static void printNPattern(int n) {
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                // Print '*' at the beginning of the row, at the diagonal, or at the end of the row
                if (j == 0 || j == n - 1 || i == j) {
                    System.out.print("*");
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println(); // Move to the next line after each row
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input the size of 'N'
        System.out.print("Enter the value of n: ");
        int n = scanner.nextInt();

        // Call the method to print the pattern
        printNPattern(n);

        scanner.close();
    }
}
  output:

Enter the value of n: 5
*   *
**  *
* * *
*  **
*   *

````

## 

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
		    for(int j=1;j<=(2*i)-1;j++){
		        if(i==1 ||i==n ||j==1 || j==(2*i)-1){
		    
		            System.out.print(" *");
		        }
		        else{
		              System.out.print("  ");
		        }
		    }
		    System.out.println();
		}
}}

output:

5
         *
       *   *
     *       *
   *           *
 * * * * * * * * *


````

## 

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
		    for(int j=1;j<=i;j++){
		    
		            System.out.print(" *");
		    }
		    System.out.println();
		}


		for(int i=1;i<=n;i++){
		    for(int j=1;j<=n;j++){
		        if(i==1 || i==n || j==1|| j==n){
		             System.out.print(" *");
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
     *
    * *
   * * *
  * * * *
 * * * * *
 * * * * *
 *       *
 *       *
 *       *
 * * * * *


````

