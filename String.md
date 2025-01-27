## Concatenate

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="Hello";
	    String str2="World";
		System.out.println("print the statement "+str1+" "+str2);
	}
}
````

##  Length of word
````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="Hello";
	    String str2="World";
	    int len=str1.length();
		System.out.println("print the statement "+str1+" "+str2);
		System.out.println("length of word "+len);
	}
}
````

## charAt Method

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="Hello";
	    String str2="World";
	    int len=str1.length();
		System.out.println("print the statement "+str1+" "+str2);
		System.out.println("length of word "+len);
	}
}

````

## Find word equals or not

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="hello world";
	    String str2="HELLO WORLD";

	 System.out.println(str1.equals(str2));
	
	}
}

````
## Convert uppercase and lowercase

````java[]


public class Main
{
	public static void main(String[] args) {
	    String str1="hello world";
	    String str2="HELLO WORLD";

	 System.out.println(str1.toUpperCase());
	 
	System.out.println(str1.toLowerCase());
	}
}

````
## IndexOf method

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="hello world";
	    String str2="HELLO WORLD";

	 System.out.println(str1.indexOf('l'));
	 

	}
}

````
## lastIndexOf Method

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="hello world";
	    String str2="HELLO WORLD";

	 System.out.println(str1.lastIndexOf('l'));
	 

	}
}
````

## startWith and endWith Method

````java[]
public class Main
{
	public static void main(String[] args) {
	    String str1="i am Nandhu";
	  

	 System.out.println(str1.startsWith("i"));
	 System.out.println(str1.endsWith("Nandhu"));

	}
}
````
## SubString Method

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="i am Nandhu";
	  

	 System.out.println(str1.substring(4));
	

	}
}

````

## replace Method

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="i am Nandhu";
	  

	 System.out.println(str1.replace('a','e'));
	

	}
}
````

## Reverse a String

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="i am Nandhu";
	    String reversed=" ";
	    for(int i=str1.length()-1;i>=0;i--){
	        reversed+=str1.charAt(i);
	    }

	 System.out.println("Reversed a String "+ reversed);
	

	}
}

output:
Reversed a String  uhdnaN ma i

````

## Find the occurance of a character in a String

````java[]

public class Main
{
	public static void main(String[] args) {
	    String str1="i am Nandhu";
	    char ch='a';
	    int count=0;
	    for(int i=0;i<str1.length();i++){
	        if(str1.charAt(i)==ch){
	            count++;
	        }
	    }

	 System.out.println("Count of character "+ count);
	

	}
}
output:
Count of character 2

````
## convert character to String

````java[]

public class Main
{
	public static void main(String[] args) {
	    char[] arr={'N','a','n','t','h','i','n','i'};
	    String str=new String(arr);
	    System.out.println("convert character to array "+str);

	

	}
}

output:
convert character to array Nanthini

````
````







