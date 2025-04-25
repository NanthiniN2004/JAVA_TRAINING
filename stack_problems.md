## Infix to Postfix Expression

````java[]

package stack;
import java.util.*;
public class Main {
	public static int prec(char c)
	{
		if (c == '^') return 3;
        else if (c == '/' || c == '*') return 2;
        else if (c == '+' || c == '-') return 1;
        else return -1;
	}
	public static String postfix(String str)
	{
		StringBuilder res=new StringBuilder();
		Stack<Character> st=new Stack<>();
		
		for(char c:str.toCharArray())
		{
			if(Character.isLetterOrDigit(c))
			{
				res.append(c);
			}
			else if(c=='(')
			{
				st.push(c);
			}
			else if(c==')')
			{
				while(!st.isEmpty() && st.peek()!='(')
				{
					res.append(st.pop());
				}
				st.pop();
			}
			else {
				while(!st.isEmpty() && prec(c)<= prec(st.peek()))
				{
					res.append(st.pop());
				}
				st.push(c);
			}
		}
		while(!st.isEmpty())
		{
			res.append(st.pop());
		}
		return res.toString();
	}

	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  System.out.println("Enter the infix expression");
	  String str=s.next();
	  String r= postfix(str);
	  System.out.println("After convert postfix expression: "+ r);
	}

}

OUTPUT:

Enter the infix expression
a+b*(c^d-e)^(f+g*h)-i
After convert postfix expression abcd^e-fgh*+^*+i-

`````
## Valid Parentheses in an Expression

````java[]

package stack;
import java.util.*;
public class Balanceparenthesis {
  public static boolean check(String str)
  {
	  Stack<Character> st=new Stack<>();
		for(int i=0;i<str.length();i++)
		{
			if(str.charAt(i)=='(' || str.charAt(i)=='{' || str.charAt(i)=='[')
			{
				st.push(str.charAt(i));
			}
			else {
				if(!st.isEmpty() && ((st.peek()=='(' && str.charAt(i)==')') 
						|| (st.peek()=='{' && str.charAt(i)=='}')
						|| (st.peek()=='[' && str.charAt(i)==']'))){
					st.pop();
					
				}
				else {
					return false;
				}
			}
		}
		return st.empty();
	}  
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		System.out.println("Enter the expression");
		String str=s.next();
		if(check(str))
		{
			System.out.println("Balanced");
		}
		else {
			System.out.println("Not balanced");
		}
		
}
}


OUTPUT:
Enter the expression
{([])}
Balanced

````


