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
## In a Text Editor Application. If you want to find and replace word in Text using replace,replaceAll,Matches
````java[]

import java.util.*;

public class Main{
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Enter the text:");
        String text = scanner.nextLine();

    
        System.out.println("Enter the word to find:");
        String find = scanner.nextLine();

        System.out.println("Enter the word to replace:");
        String replace = scanner.nextLine();

        String replacedText = text.replace(find, replace);
        System.out.println("After Replace the character");
        System.out.println(replacedText);

    
        String regex = "\\b" + find + "\\b"; 
        String replacedalltext = text.replaceAll(regex, replace);
        System.out.println("Using replaceAll method:");
        System.out.println(replacedalltext);
        
        System.out.println("Using matches method:");
        if (text.matches(".*\\b" + find + "\\b.*")) {
            System.out.println("The word \"" + find + "\" was found in the text.");
        } else {
            System.out.println("The word \"" + find + "\" was not found in the text.");
        }

        scanner.close();
    }
}

output:
Enter the text:
java is object oriented programming language.
Enter the word to find:
object
Enter the word to replace:
obj
After Replace the character
java is obj oriented programming language.
Using replaceAll method:
java is obj oriented programming language.
Using matches method:
The word "object" was found in the text.
````

## develop a login system and need to validate the user credential using string method stim, equal, equalignorecase

````java[]
import java.util.*;

public class Main{
    public static void main(String[] args) {
    
        String username = "Admin";
        String password = "Pass123";

        Scanner scanner = new Scanner(System.in);

    
        System.out.println("Welcome to the Login System!");
        System.out.print("Enter your username: ");
        String un = scanner.nextLine().trim(); 

        System.out.print("Enter your password: ");
        String pw= scanner.nextLine().trim(); 

        
        System.out.println("Validation Results:");

        
        if (un.equals(username) && pw.equals(password)) {
            System.out.println("Login successful (exact match with equals).");
        } else {
            System.out.println("Login failed (case-sensitive comparison).");
        }

        if (un.equalsIgnoreCase(username) && pw.equals(password)) {
            System.out.println("Login successful (username case-insensitive with equalsIgnoreCase).");
        } else {
            System.out.println("Login failed (case-insensitive username comparison).");
        }

        System.out.println("\nDebugging Info:");
        System.out.println("Entered Username (after trim): '" + un + "'");
        System.out.println("Entered Password (after trim): '" + pw + "'");

        scanner.close();
    }
}

````









