using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

class Program
{
    static void Main(string[] args)
    {
        int number = 0;
        int counter = 0;
        int p = 1;
        bool isEqual = false;
        Console.Write("0, 1, ");
        while (counter < 128)
        {
            string numberString = number.ToString();
            string numberBinary = Convert.ToString(number, 2);
            if (number < 10)
            {
                for (int i = 0; i < numberBinary.Length / 2; i++)
                {
                    if (numberBinary[i] == numberBinary[numberBinary.Length - p])
                    {
                        isEqual = true;
                    }
                    else
                    {
                        isEqual = false;
                        break;
                    }
                    p++;
                    if (numberBinary[i] == numberBinary[numberBinary.Length / 2 - 1])
                    {
                        Console.Write("{0}, ", number);
                        counter++;
                    }
                }
                p = 1;
            }
            else
            {
                for (int i = 0; i < numberBinary.Length / 2; i++)
                {
                    if (numberBinary[i] == numberBinary[numberBinary.Length - p])
                    {
                        isEqual = true;
                    }
                    else
                    {
                        isEqual = false;
                        break;
                    }
                    p++;
                }
                p = 1;
                if (isEqual == true)
                {
                    for (int i = 0; i < numberString.Length / 2; i++)
                    {
                       if (numberString[i] == numberString[numberString.Length - p])
                       {
                           isEqual = true;
                       }
                       else
                       {
                           isEqual = false;
                           break;
                       }
                       p++;
                    }
                    if (isEqual == true)
                    {
                        Console.Write("{0}, ", number);
                        counter++;
                    }
                }
            }
            number++;
            p = 1;
        }
    }
}
