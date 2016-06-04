# Palindromesusing System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


class Program
{
    static void Main(string[] args)
    {
        int[] numbers = Console.ReadLine().Split().Select(int.Parse).ToArray();
        int start = 0;
        int len = 1;
        int pos = 1;
        int bestStart = 0;
        int bestLen = 0;
        for (int i = 0; i < numbers.Length - 1; i++)
        {
            pos = i;
            if (numbers[i] == numbers[i + 1] - 1)
            {
                len++;
                if (bestLen < len)
                {
                    bestStart = start;
                    bestLen = len;
                }
            }
            else
            {
                len = 1;
                start = pos + 1;
            }
        }
        int[] result = new int[bestLen];
        for (int i = 0; i < bestLen; i++)
        {
            result[i] = numbers[bestStart + i];
        }
        Console.WriteLine(string.Join(" ", result));
    }
}
