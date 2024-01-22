# 5
using System;

class Program
{
    static void Main()
    {
        int[] numbers = { 1, 2, 3 };

        try
        {
            // Attempting to access an element outside the valid range
            Console.WriteLine("Trying to access an element outside the valid range...");
            int value = numbers[5]; // This will cause an IndexOutOfRangeException
            Console.WriteLine($"Value at index 5: {value}"); // This line will not be executed
        }
        catch (IndexOutOfRangeException ex)
        {
            // Catch block will execute if an IndexOutOfRangeException occurs
            Console.WriteLine($"Caught an exception: {ex.GetType().Name}");
            Console.WriteLine("Index is out of bounds!");
        }
        finally
        {
            // Finally block will always execute, regardless of whether an exception occurred or not
            Console.WriteLine("Finally block is executed");
        }

        // This line will be executed after the try-catch-finally blocks
        Console.WriteLine("Program continues after exception handling");
    }
}
