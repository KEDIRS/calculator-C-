
using System;

class Calculator
{
    static void Main(string[] args)
    {
        Console.WriteLine("Simple Calculator");
        Console.WriteLine("-----------------");
        Console.WriteLine("Enter the first number:");
        double num1 = Convert.ToDouble(Console.ReadLine());

        Console.WriteLine("Enter the operator (+, -, *, /):");
        char op = Console.ReadLine()[0];

        Console.WriteLine("Enter the second number:");
        double num2 = Convert.ToDouble(Console.ReadLine());

        double result = 0;

        switch (op)
        {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 * num2;
                break;
            case '/':
                if (num2 != 0)
                {
                    result = num1 / num2;
                }
                else
                {
                    Console.WriteLine("Error: Division by zero is not allowed.");
                    return;
                }
                break;
            default:
                Console.WriteLine("Invalid operator.");
                return;
        }

        Console.WriteLine($"Result: {num1} {op} {num2} = {result}");
    }
}
