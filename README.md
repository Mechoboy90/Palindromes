using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

class Program
{
    static void Main(string[] args)
    {
        short cen = short.Parse(Console.ReadLine());
        int years = cen * 100;
        double days = years * 365.24;
        int hours = (int)days * 24;
        int minutes = hours * 60;
        ulong seconds = (ulong)minutes * 60;
        ulong milliseconds = seconds * 1000;
        ulong microseconds = milliseconds * 1000;
        ulong nanoseconds = milliseconds * 1000;
        Console.WriteLine("{0} centuries = {1} years = {2} days = {3} hours = {4} minutes = {5} seconds = {6} milliseconds = {7} microseconds = {8} nanoseconds", cen, years, days, hours, minutes, seconds, milliseconds, microseconds, nanoseconds);

    }
}
