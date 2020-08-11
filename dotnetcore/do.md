dotnet new console --output sample1   
dotnet run --project sample1   

dotnet new console   
dotnet run   
 
```C#
            Console.WriteLine("\nWhat is your name? ");
            var name = Console.ReadLine();
            var date = DateTime.Now;
            Console.WriteLine($"\nHello, {name}, on {date:d} at {date:t}!");
            Console.Write("\nPress any key to exit...");
            Console.ReadKey(true);
```   

dotnet run --configuration Release   

dotnet publish --configuration Release   

dotnet HelloWorld.dll   


dotnet new sln   

dotnet new classlib -o StringLibrary   

dotnet sln add StringLibrary/StringLibrary.csproj   


```C#
using System;

namespace UtilityLibraries
{
    public static class StringLibrary
    {
        public static bool StartsWithUpper(this String str)
        {
            if (String.IsNullOrWhiteSpace(str))
                return false;

            Char ch = str[0];
            return Char.IsUpper(ch);
        }
    }
}
```   

dotnet build   

dotnet new console -o ShowCase   

dotnet sln add ShowCase/ShowCase.csproj   

```C#
using System;
using UtilityLibraries;

class Program
{
    static void Main(string[] args)
    {
        int row = 0;

        do
        {
            if (row == 0 || row >= 25)
               ResetConsole();

            string input = Console.ReadLine();
            if (String.IsNullOrEmpty(input)) break;
            Console.WriteLine($"Input: {input} {"Begins with uppercase? ",30}: " +
                              $"{(input.StartsWithUpper() ? "Yes" : "No")}\n");
            row += 3;
        } while (true);
        return;

        // Declare a ResetConsole local method
        void ResetConsole()
        {
            if (row > 0) {
               Console.WriteLine("Press any key to continue...");
               Console.ReadKey();
            }
            Console.Clear();
            Console.WriteLine("\nPress <Enter> only to exit; otherwise, enter a string and press <Enter>:\n");
            row = 3;
        }
    }
}
```
