C# Basics exam April 2015

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _Problem.03: King of Thieves
{
    class Program
    {
        static void Main()
        {
//Once upon a time there was a kingdom and everyone in the kingdom was a thief. Izzy wanted to become the King of Thieves and so started stealing only perfect gems from other thieves. Help Izzy by showing him what a perfect gem with given parameters should look like.
//Input
//The input data should be read from the console. 
//•	The first line will hold the size of the gem – n.
//•	The second line will hold the type of the gem – a symbol: e.g. ‘*’.
//The input data will always be valid and in the format described. There is no need to check it explicitly.
//Output
//The output should be printed on the console. It should consist of ‘n’ lines, holding the gem.

            int n = int.Parse(Console.ReadLine());
            char enterSymbol = char.Parse(Console.ReadLine());
            
            for (int i = 1; i <= n; i += 2)
            {
                int dashes = (n - i) / 2;
                int symbol = i;
                
                Console.Write(new string('-', dashes));
                Console.Write(new string(enterSymbol, symbol));
                Console.Write(new string('-', dashes));
                Console.WriteLine();
            }
            for (int i = n - 2; i >= 1; i -= 2)
            {
                int dashes = (n - i) / 2;
                int symbol = i;
                Console.Write(new string('-', dashes));
                Console.Write(new string(enterSymbol, symbol));
                Console.Write(new string('-', dashes));
                Console.WriteLine();

            }
        }
    }
}
