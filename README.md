# cash-project
import java.util.Scanner;

/* programmers: Collin Palmer,Zachariah Pelletier
 * Date:09/28/16
 * COSC 111 MW 2:00
 * Khaled Mansour
 * Purpose: A self working cash register that calculates the amount due 
 * back after the amount is tendered and
 *  give a break down of the type of change they will receive.
 */
	public class cash 
{
   
	public static void main(String[] args)
	{
	        Scanner k =new Scanner(System.in);
		    double amounttend=0.0;
		    double totalchange =0.0;
		    double totalchangef=0.0;
		    int dollars=0;
		    int quarters=0;
		    int dimes=0;
		    int nickels=0;
		    int cents=0;
		    double amountsale=0.0;
		    int hundred=100;
		    int leftover=0;
		    int twentyfive=25;
		    int ten=10;
		    int five=5;
		    
		    
		    
		    System.out.println("Enter amount of sale:");
		    amountsale=k.nextDouble();
		    
		    System.out.println("Enter amount tendered by customer:");
		    amounttend=k.nextDouble();
		    
		    totalchange=(amounttend-amountsale);
		    totalchangef=(totalchange*hundred);
		    totalchange=Math.floor(totalchange *hundred) / hundred;
		    dollars= (int)(totalchangef/hundred);
		    leftover= (int)(totalchangef%hundred);
		    quarters=(leftover/twentyfive);
		    leftover=(leftover%25);
		    dimes=(leftover/ten);
		    leftover=(leftover%ten);
		    nickels=(leftover/five);
		    leftover=(leftover%five);
		    cents=leftover;
		    
		    
		    System.out.println("Total change	=$"+totalchange);
		    System.out.println("Dollars\t\t="+dollars);
		    System.out.println("Quarters\t="+quarters);
		    System.out.println("Dimes   \t="+dimes);
		    System.out.println("Nickels \t="+nickels);
		    System.out.println("Cents\t\t="+cents);
		    System.out.println("Thanks you for using Collin Palmer Cash register program");
		    
	}

}
