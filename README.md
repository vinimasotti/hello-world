# hello-world
Just another repository
.
.
.
.

using System;

namespace TaskTwoViniciusBianchi

{
	class Program //class is a central feature of OOP
	{
		public static void Main(string[] args)
		{
			Console.WriteLine("--- TASK TWO --- ");

			BankAccount VinnyAccount = new BankAccount(); //new object, object = block of memory
			VinnyAccount.OpenBankAccount(); //calling method OpenBankAccount
			VinnyAccount.DisplayAccount(); //calling metthod DisplayAccount

			Console.Write("Press any key to continue . . . ");
			Console.ReadKey(true);
		}
	}

public class BankAccount 
	{
		//two member fields. privates cant be accessed in other classe while public yes
		private decimal accountnumber;
		private decimal Balance;

		public  BankAccount() //overload constructor

		{
			accountnumber = 0;
			Balance = 0;
		}

		public void OpenBankAccount() // method to open a bank account, interacting with user
		{
			Console.WriteLine("Enter Account Number");
			decimal OpenAccountnumber = Convert.ToDecimal(Console.ReadLine());
			Console.WriteLine("Enter opening balance");
			decimal OpeningBalance = Convert.ToDecimal(Console.ReadLine());
			Balance = OpeningBalance; //store Balance inputed from user
            accountnumber = OpenAccountnumber; //store account number inputed from user 
		}
		public void Deposit(decimal amount) //method to record deposits to bank account.
		{
			Balance += amount;
		}
		public void DisplayAccount() // method for displaying account number and ballance 
		{
			Console.WriteLine("Your Account number: " + accountnumber);
			Console.WriteLine("Your Balance " + Balance);

		}
	}
}
