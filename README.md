/*
Unit 10: Coding Project
For this coding exercise, you will implement the recursive method fibonacci(int n) that will return the nth number of the Fibonacci sequence. Recall that the Fibonacci sequence is the previous two numbers added to get the next number. The first two numbers of Fibonacci are 1 and 1 (the 0th term would be 0).

Example:
fibonacci(5)
 
5
 
Sequence:
1,1,2,3,5

Your code will run against tests to see if it is correct. Once all tests pass, then you have successfully completed this project!

Hints:
If Fibonacci relies on the previous two numbers, how can we break this down into a smaller problem?
Make sure to include a base case that covers an input of 0 or 1.
*/
import java.util.*;

class Unit10 {
    public long fibonacci(int n) {
        if(n == 0){
            return 0;
        }
        else if(n == 1){
            return 1;
        }
        else{
            return fibonacci(n - 1) + fibonacci(n - 2);
        }
    }
}

public class Main
{
	public static void main(String[] args) {
	    Scanner s = new Scanner(System.in);
		Unit10 unit = new Unit10();
		int input = s.nextInt();
		long result = unit.fibonacci(input);
		System.out.println("The result is: " + result);
	}
}
