using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Fox
{
    class Fox
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());
            int middle = (n * 2) - 1;
            int side = n / 2;
            int m = n;

            for (int i = 1; i <= n; i++)
            {
                Console.WriteLine("{0}\\{1}/{0}", new string('*', i), new string('-', middle));
                middle -= 2;
            }

            for (int i = 0; i < n / 3; i++)
            {
                Console.WriteLine("|{0}\\{1}/{0}|", new string('*', side), new string('*', m));
                m -= 2;
                side++;
            }


            int middleDown = (n * 2) - 1;

            for (int j = 1; j <= n; j++)
            {
                Console.WriteLine("{0}\\{1}/{0}", new string('-', j), new string('*', middleDown));
                middleDown -= 2;
            }
        }
    }
}
