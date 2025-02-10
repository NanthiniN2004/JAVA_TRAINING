## BINARY SEACH
````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int[] a=new int[n];
		System.out.println("Enter the element");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		System.out.println("Enter the target");
		int target=s.nextInt();
		int start=0;
		int end=a.length-1;
		int flag=0;
		while(start<=end){
		    int mid=(start+end)/2;
		    if(a[mid]==target){
		        flag=1;
		        System.out.println("Element Found: "+mid);
		        break;
		    }
		    else if(a[mid]<target){
		        start=mid+1;
		    }
		    else{
		        end=mid-1;
		    }
		}
		if(flag==0){
		    System.out.println("Element Not found");
		}
	}
}


OUTPUT:

Enter the size of the arra
5
Enter the element
20
30
40
50
60
Enter the target
50
Element Found: 3


````
