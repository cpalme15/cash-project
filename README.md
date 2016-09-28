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
		    char C;
		    
		    
		    System.out.printf("Enter amount of sale:%16s","$");
		    amountsale=k.nextDouble();
		     
		    
		    System.out.printf("Enter amount tendered by customer:%3s","$");
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
		    
		    
		    System.out.printf("Total change %9s","=$"+totalchange);
		    System.out.printf("\nDollars%11s","="+dollars);
		    System.out.printf("\nQuarters%10s","="+quarters);
		    System.out.printf("\nDimes%13s","="+dimes);
		    System.out.printf("\nNickels%11s","="+nickels);
		    System.out.printf("\nCents%13s","="+cents);
		    System.out.printf("\nThanks you for using Collin Palmer Cash register program");
		    
	}

}
