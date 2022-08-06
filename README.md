# Stacks-and-its-operations
import java.util.Stack;
public class Q1 {
	class Stack{
		private int arr[];
		private int top;
		private int capacity;
		//constructor to initialize the stack
		Stack(int size){
			arr=new int[size];
			capacity=size;
			top=-1;
		}
		//utility function to add an element 'x' t the stack
		public void push(int x)
		{
			if (isFull())
			{
				System.out.println("Overlow\nProgram Terminated\n");
			System.exist(-1);
			}
			System.out.println("inserting"+x);
			arr[++top]=x;
			}
			//utility function to pop a top element from the stack 
		public int pop()
		{
			//check for stack underflow
			if(isEmpty()) {
				System.out.println("underflow\nProgram Terminated")
				System.exist(-1);
			}
			System.out.println("removing"+ peek());
		//decrease stack size by 1 and (optionally) return the popped element
		return arr[top--];	
		}
		//utility function to return top elemet of the stack
		public int peek()
		{
			if(!isEmpty()) {
				return arr[top];
			}
			else {
				System.exist(-1);
			}
		return -1;
		}
		//utility fuctio to return the size of the stack
	public int size() {
		return top +1;
	}	
		//utility function to check if the stac iss empt or not
	public boolean isEmpty() {
		return top==-1;
	}
	//utility function to check if the stack is full or not
public boolean idFull() {
	return top==capacity-1 ;
}	
		}
class Main{
	public static void main(String[] args) {
	Stack stack=new Stack(3);
	stack.push(1);
	stack.push(2);
	stack.pop();
	stack.pop();
	stack.push(3);
	System.out.println("the top element is" +stack.peek());
	System.out.println("the stack size is"+ stack.size());
	stack.pop();
	if(stack.isEmpty()) {
		System.out.println("the stack is empty");
	}
}
	}
}


import java.util.Stack;
public class Q2 {
	public static void reverse(char[] c)
	{
		//create an empty stack of chracter
		Stack<Character> stack=new Stack<>();
	//push each character 
		for(int  i=0; i<c.length; i++) {
			stack.push(c[i]);
		}
		//start from index 0
		int k=0;
		//pop characters from the stack until its empty
		while(!stack.empty())
		{
			//assign each popped character back to input string
		c[k++]=stack.pop();	
		}
	}
	public static void main(String[] args) {
	String str="welcome to usman institute of technology 2022";
	char[] c=str.toCharArray();
	reverse(c);
	str=new String(c);
	System.out.println("reverse of the give string is "+str);
}
}
