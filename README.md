Target-Number
=============
import java.util.ArrayList;
import java.util.Scanner;


public class tracer 
{
	public static int name,left, right, middle, middleNum, target, middleGuess;
	public static String answer, going;

	public static void main(String[] args) 
	{
		ArrayList bubbles = new ArrayList();
		
		do
		{
			System.out.println("Enter Numbers?");
			Scanner userinput = new Scanner(System.in);
			answer = userinput.nextLine();
			if (answer.equals("yes"))
			{
		    System.out.println("Enter a number between 1 -20");
			name = userinput.nextInt();
			bubbles.add(name);
			}
		}
		while(answer.equals("yes"));
			
		System.out.println(bubbles);
		
		System.out.println("Enter Target Number");
		Scanner userinput5 = new Scanner(System.in);
		target = userinput5.nextInt();
		
		System.out.println("Enter left spot?");
		Scanner userinput1 = new Scanner(System.in);
		left = userinput1.nextInt();
		if(left == 0)
		{
			System.out.println("Correct");
		}
		else
		{
			System.out.println("Incorrect");
		}
		System.out.println("Enter right spot?");
		right = userinput1.nextInt();
		if(right == bubbles.size()-1)
		{
			System.out.println("Correct");
		}
		else
		{
			System.out.println("Incorrect");
		}
		System.out.println("Enter middle spot?");
		middleGuess = userinput1.nextInt();
		if(middleGuess == (left + right)/2)
		{
			System.out.println("Correct");
		}
		else
		{
			System.out.println("Incorrect");
		}
		System.out.println("Enter middle number?");
		middleNum = userinput1.nextInt();
		middle = left + right / 2;
		if(middleNum == (int) bubbles.get(middle))
		{
			System.out.println("Correct");
		}
		else
		{
			System.out.println("Incorrect");
		}

		
		
		System.out.println("Keep Going?");
		Scanner userinput3 = new Scanner(System.in);
		going = userinput3.nextLine();
		
		if(going.equals("yes"))
		{
			do
			{
				
			System.out.println(bubbles);
			
			System.out.println("Enter left spot?");
			Scanner userinput4 = new Scanner(System.in);
			left = userinput4.nextInt();
			if(left < middle && target > middle)
			{
				if(left == middle)
				System.out.println("Correct");
				
				else 
				{
					System.out.println("Incorrect");
				}
			}
			else if(left < middle && target < middle)
			{
				if(left == 0)
					System.out.println("Correct");
				else
				System.out.println("Incorrect");
			}
			System.out.println("Enter right spot?");
			right = userinput4.nextInt();
			if(right > middle && middle < target)
			{
				if(right == bubbles.size())
				System.out.println("Correct");
				
				else
					System.out.println("Incorrect");
			}
			else if(right > middle && middle > target)
			{
				if(right == middle)
					System.out.println("Correct");
				
				else
				System.out.println("Incorrect");
			}
			System.out.println("Enter middle spot?");
			middleGuess = userinput4.nextInt();
			if(middleGuess == (left + right)/2)
			{
				System.out.println("Correct");
			}
			else
			{
				System.out.println("Incorrect");
			}
			System.out.println("Enter number in the middle spot?");
			middleNum = userinput4.nextInt();
			
			middle = left + right / 2;
			if(middleNum == (int) bubbles.get(middle))
			{
				System.out.println("Correct");
			}
			else
			{
				System.out.println("Incorrect");
			}
			
			}
			while(going.equals("yes"));
		}	
	}

}
