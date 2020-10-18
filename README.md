//Diego Grisales
//Commission calculator by employee for Celldistributions.Corp
//09/25/2020

import java.util.Scanner;

public class Commissions {
	
	Commissions() {
		
		System.out.println("Monthly commission calculator by employee \nPlease enter the following information. ");
		
		Scanner inp = new Scanner(System.in);
		
		String employee;
		System.out.print("\nEmployee's name: ");
		employee = inp.next();
		
		double autopay;
		System.out.print("\nNumber of autopay assigned: ");
		autopay = inp.nextDouble();
		
		double reactAndByod;
		System.out.print("Number of reactivations or BYOD: ");
		reactAndByod = inp.nextDouble();
		reactAndByod = reactAndByod * 5;
		
		double newAcct60;
		System.out.print("NEW accounts sold with $60 plan: ");
		newAcct60 = inp.nextDouble();
		
		char goal60; 
		System.out.print("Type 'a' for goal A or 'b' for goal B: ");
		goal60 = inp.next(".").charAt(0);
		
		if (goal60 == 'a') {
			newAcct60 = newAcct60 * 4;
		}
		else if (goal60 == 'b') {
			newAcct60 = newAcct60 * 6;
		} 
		
		double newAcct;
		System.out.print("NEW accounts sold with other plans: ");
		newAcct = inp.nextDouble();
		
		char goal; 
		System.out.print("Type 'a' for goal A or 'b' for goal B: ");
		goal = inp.next().charAt(0);
		
		if (goal == 'a') {
			newAcct = newAcct * 3;
		}
		else if (goal == 'b') {
			newAcct = newAcct * 5;
		}
		
		double upgrade;
		System.out.print("Number of upgrades sold: ");
		upgrade = inp.nextDouble();
		upgrade = upgrade * 5;
		
		double iot;
		System.out.print("Number of IOTs sold: ");
		iot = inp.nextDouble();
		iot = iot * 5;
		
		double accessories;
		System.out.print("Amount in dollars sold in accessories, (example $1,000 = 1000): ");
		accessories = inp.nextDouble();
		
		char accGoal;
		System.out.print("Type 'a' for goal A, 'b' for goal B, or 'c' for goal C: ");
		accGoal = inp.next().charAt(0);
		
		if (accGoal == 'a') {
			accessories = accessories * .10;
		}
		else if (accGoal == 'b') {
			accessories = accessories * .13;
		}
		else if (accGoal == 'c') {
			accessories = accessories * .18;
		}
		
		double monthTotal = autopay + reactAndByod + newAcct60 + newAcct + upgrade + iot + accessories;
		
		System.out.println("\nRetention comissions for past months: ");
		
		double storeSales1;
		System.out.print("Number of phones with NEW ACCOUNTS on the first month (store total): ");
		storeSales1 = inp.nextDouble();
		
		double retention1;
		System.out.print("STORE retention percentage for the first month, (example 70% = .70): ");
		retention1 = inp.nextDouble();
		
		double sales1;
		System.out.print("EMPLOYEE's percentage of sales on the first month, (example 40% = .40): ");
		sales1 = inp.nextDouble();
		sales1 = sales1 * storeSales1;
		
		double month1; 
		month1 = retention1 * sales1 * 1.00;
		
		
		
		
		double storeSales2;
		System.out.print("\nNumber of phones sold with NEW accounts on the second month: ");
		storeSales2 = inp.nextDouble();
		
		double retention2;
		System.out.print("STORE retention percentage for the second month, (example 70% = .70): ");
		retention2 = inp.nextDouble();
		
		double sales2;
		System.out.print("EMPLOYEE's percentage of sales on the second month, (example 40% = .40): ");
		sales2 = inp.nextDouble();
		sales2 = sales2 * storeSales2;
		
		double month2; 
		month2 = retention2 * sales2;
		
		
		double storeSales3;
		System.out.print("\nNumber of phones sold with NEW accounts on the third month: ");
		storeSales3 = inp.nextDouble();
		
		double retention3;
		System.out.print("STORE retention percentage for the third month, (example 70% = .70): ");
		retention3 = inp.nextDouble();
		
		double sales3;
		System.out.print("EMPLOYEES's percentage of sales on the third month, (example 40% = .40): ");
		sales3 = inp.nextDouble();
		sales3 = sales3 * storeSales3;
		
		double month3; 
		month3 = retention3 * sales3;
		
		
		double storeSales4;
		System.out.print("\nNumber of phones sold with NEW accounts on the fourth month: ");
		storeSales4 = inp.nextDouble();
		
		double retention4;
		System.out.print("STORE retention percentage for the fourth month, (example 70% = .70): ");
		retention4 = inp.nextDouble();
		
		double sales4;
		System.out.print("EMPLOYEE's percentage of sales on the second fourth, (example 40% = .40): ");
		sales4 = inp.nextDouble();
		sales4 = sales4 * storeSales4;
		
		double month4; 
		month4 = retention4 * sales4;
		
		
		double storeSales5;
		System.out.print("\nNumber of phones sold with NEW accounts on the fifth month: ");
		storeSales5 = inp.nextDouble();
		
		double retention5;
		System.out.print("STORE retention percentage for the fifth month, (example 70% = .70): ");
		retention5 = inp.nextDouble();
		
		double sales5;
		System.out.print("EMPLOYEE's percentage of sales on trun he fifth month (example 40% = .40): ");
		sales5 = inp.nextDouble();
		sales5 = sales5 * storeSales5;
		
		double month5; 
		month5 = retention5 * sales5; 
		inp.close();
		
		double totalRetention = month1 + month2 + month3 + month4 + month5;
		
		System.out.println("\n" + employee + "'s commissions: \n\nAutopay: $" + autopay + "\nReactivations/BYOD: $" 
				+ reactAndByod + "\nNew $60 plan accounts: $" + newAcct60 + "\nNew $50 plan accounts: $" +
				newAcct + "\nUpgrades: $" + upgrade + "\nIOT: $" + iot + "\nAccessories: $" + accessories);
		
		System.out.printf("\nTotal commissions for this month: $" + "%.2f", monthTotal);
		
		System.out.printf("\nRetention for the first month is: $" + "\nRetention for the second month is: $" 
				+ month2 + "\nRetention for the third month is: $" + month3 + "\nRetention for the fourth month is: $" 
				+ month4 + "\nRetention for the fifth month is: $" + month5 + "\n" + "Total retention for past 5 months: $"
		 		 + "%.2f", totalRetention);  
		
		double finalCommissions;
		finalCommissions = monthTotal + totalRetention;
		System.out.printf("\n" + employee + "'s total commissions for this month plus retention for past months: $" 
		+ "%.2f", finalCommissions);
		
		}

	public static void main(String[] args) {
		
		Commissions obj;
		obj = new Commissions();
		System.out.println("\n\n\n\n" + obj);
	}
}
