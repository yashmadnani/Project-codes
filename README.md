

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


//C# program to order coffee and display Bill amount 
//Using Switch 
namespace T17
{
    class Program
    {
        static void Main()
        {
            int TotalCoffeeCost = 0;
        start:
            Console.WriteLine("Please select your Coffee size : 1-Small , 2-Medium , 3-Large");
            int userChoice = int.Parse(Console.ReadLine());

            switch (userChoice)
            {
                case 1:
                    TotalCoffeeCost += 1;
                    break;
                case 2:
                    TotalCoffeeCost += 2;
                    break;
                case 3:
                    TotalCoffeeCost += 3;
                    break;
                default:
                    Console.WriteLine("Your Choice {0} is invalid", userChoice);
                    goto start;
            }

        Decide:
            Console.WriteLine("Do you want to buy another Coffee - Yes or No");
            string userDecision = Console.ReadLine();

            switch (userDecision.ToUpper())
            {
                case "YES":
                    goto start;
                case "NO":
                    break;
                default:
                    Console.WriteLine("Your Choice {0} is invalid, try again" , userDecision);
                    goto Decide;


            
        }
        Console.WriteLine("Thank you for shopping");
            Console.WriteLine("Bill amount =  ${0}", TotalCoffeeCost);

            Console.Read();

        }

     }
}
