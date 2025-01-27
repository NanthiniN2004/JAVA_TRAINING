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

## Find Index of character

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
## Convert upper case and lowercase

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


