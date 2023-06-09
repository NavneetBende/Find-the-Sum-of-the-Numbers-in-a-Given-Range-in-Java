# Find-the-Sum-of-the-Numbers-in-a-Given-Range-in-Java

Find the Sum of the Numbers in a Given Range in Java
Find the Sum of the Numbers in a Given Range in Java
Find the Sum of the Numbers in a Given Range in Java
Given two integer inputs number1 and number2, the objective is to find the sum of all Number that lay in the given interval by writing a code to Find the Sum of the Numbers in a Given Range in Java Language.

Example
Input : Number1 = 12 , Number2 = 15
Output : 54
Find the Sum of the Numbers in a Given Interval in Java
Given the range as integer input, the objective is to find the Sum of all the Numbers that lay in the given interval using different methods. To do so we basically iterate from the base interval to the final interval and keep adding the number. Here are some of the methods to solve the above mentioned problem in Java Language.

Method 1: Using Brute Force
Method 2: Using the Formula
Method 3: Using Recursion
We’ll discuss the above mentioned methods in detail in the upcoming sections.

Related Pages
Greatest of two numbers

Greatest of the Three numbers

Leap year or not

Prime number

Prime number within a given range

Method 1: Using Brute Force
In this method we’ll use loops to iterate through from the base interval to the upper interval meanwhile adding all the numbers to the sum variable.

Working
For the given integer input intervals number1 and number2

Initialize the required variables.
Initiate a for loop from range [5,10].
Keep adding the value of the iter variable to sum variable.
Print the sum variable.
Let’s implement the above working in Java Language.

Java Code
public class Main
{
  public static void main (String[]args)
  {
    int a = 5;
    int b = 10;

    int sum = 0;

    for (int i = a; i <= b; i++)
        sum = sum + i;
      System.out.println ("The sum is " + sum);
  }
}
Output
The sum is 45
Method 2: Using the Formula
In this method we’ll use a sequence and series formula to find the sum of n numbers in a series. Formula : N*(N+1)/2.

Working
For the given integer input intervals number1 and number2

Initialize the required variables.
Apply the given formula sum = b*(b+1)/2 – a*(a+1)/2 + a.
Print the sum variable as output.
Let’s implement the above working in Java Language.

Java Code
public class Main
{
	public static void main(String[] args) {
	    int num1 = 2;
	    int num2 = 5;
	    int sum = num2*(num2+1)/2 - num1*(num1+1)/2 + num1;
		System.out.println("The Sum is "+ sum);
	}
}
Output
The Sum is 14
Method 3: Using Recursion
In this method we’ll use recursion to iterate through and sum up all the numbers that lay in the given interval.

Working
For the Integer inputs number1 and number2

Initialize the required variable sum = 0.
Define a recursive function with base case as number1 == number2.
Set the recursive set call as num1+ function(sum,num1+1,num2).
print the returned value after calling the recursive functions.
Let’s implement the working in Java Language.

Java Code
public class Main
{
  public static void main (String[]args)
  {
    int a = 5;
    int b = 10;

    int sum = getSum (0, a, b);
      System.out.println ("The sum is " + sum);
  }


  static int getSum (int sum, int i, int b)
  {

    // stop when any recursion call tries to go over b (larger number)
    if (i > b)
      return sum;

    return i + getSum (sum, i + 1, b);
  }
}
Output
The Sum is 45
