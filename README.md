# Module-4-Project
This is a GitHub Repository Assignment for the project of COP2360-1 Module 4

using System;

//namespace CSharpDivisionApp
//{
  class Program
  {
    static void Main()
    {
      Console.Write ("Enter two numbers: ");
      string input1 = Console.ReadLine();

      //Console.Write ("Enter the second number: ");
      string input2 = Console.ReadLine();

        int n1 = Convert.ToInt32(input1);
        int n2 = Convert.ToInt32(input2);

        int sum = n1 + n2;
        Console.WriteLine($"The sum of {n1} plus {n2} is: {sum}"); 
      
      Console.Write ("Enter the first number: ");
      string strInput1 = Console.ReadLine();

      Console.Write ("Enter the second number: ");
      string strInput2 = Console.ReadLine();

      try
      {
        int num1 = Convert.ToInt32(strInput1);
        int num2 = Convert.ToInt32(strInput2);

        int result = DivideStrings(strInput1, strInput2);
        Console.WriteLine($"The result of {num1} divided by {num2} is: {result}"); 
      }
      catch (FormatException e)
        {
          Console.WriteLine("Incorrect FormatException! One or both of the inputs are not valid integers.");
          Console.WriteLine($"Detailed error message: {e.Message}");
        }
      catch (DivideByZeroException ex)
      {
          Console.WriteLine("Error! Number cannot divided by zero.");
          Console.WriteLine($"Detailed error message: {ex.Message}");
      }
      try
      {
        int num1 = Convert.ToInt32(strInput1);
        int num2 = Convert.ToInt32(strInput2);

        int result = DivideStrings(strInput1, strInput2);
        Console.WriteLine($"The result of {num1} divided by {num2} is: {result}");
        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
      }
      catch (Exception iex)
      {
          Console.WriteLine("Stop! An error unexpectedly occurred in the solution.");
          Console.WriteLine($"Detailed error message: {iex.Message}");
      }
    }
    static int DivideStrings(string number1, string number2)
    {
      int input1 = int.Parse(number1);
      int input2 = int.Parse(number2);

      if (input2 == 0)
      {
        throw new DivideByZeroException("Division by zero is not allowed.");
      }
      
      return input1 / input2;
    }
  }
//}
