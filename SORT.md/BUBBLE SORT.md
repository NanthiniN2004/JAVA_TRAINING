## BUBBLE SORT
````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	   Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		int[] a=new int[n];
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		bubblesort(a,n);
			for(int i=0;i<n;i++){
		    System.out.print(a[i]+" ");
		}
		
	}
	public static void bubblesort(int[] a,int n){
		for(int i=0;i<n;i++){
		    for(int j=i;j<n-1-i;j++){
		        if(a[j]>a[j+1]){
		            int temp=a[j];
		            a[j]=a[j+1];
		            a[j+1]=temp;
		        }
		    }
		}
	
	}
}


OUTPUT:

5
3
1
5
2
4
1 2 3 4 5

````

