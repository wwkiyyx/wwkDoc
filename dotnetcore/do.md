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

