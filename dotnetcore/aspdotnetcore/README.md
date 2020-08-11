# Razor Pages

dotnet new webapp -o RazorPagesMovie   

code -r RazorPagesMovie   

dotnet dev-certs https --trust   

```C#
using System;
using System.ComponentModel.DataAnnotations;

namespace RazorPagesMovie.Models
{
    public class Movie
    {
        public int ID { get; set; }
        public string Title { get; set; }

        [DataType(DataType.Date)]
        public DateTime ReleaseDate { get; set; }
        public string Genre { get; set; }
        public decimal Price { get; set; }
    }
}
```   

dotnet tool install --global dotnet-ef   
dotnet tool install --global dotnet-aspnet-codegenerator   
dotnet add package Microsoft.EntityFrameworkCore.SQLite   
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design   
dotnet add package Microsoft.EntityFrameworkCore.Design   
dotnet add package Microsoft.EntityFrameworkCore.SqlServer   

```C#
using Microsoft.EntityFrameworkCore;

namespace RazorPagesMovie.Data
{
    public class RazorPagesMovieContext : DbContext
    {
        public RazorPagesMovieContext (
            DbContextOptions<RazorPagesMovieContext> options)
            : base(options)
        {
        }

        public DbSet<RazorPagesMovie.Models.Movie> Movie { get; set; }
    }
}
```   

{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
  "AllowedHosts": "*",
  "ConnectionStrings": {
    "MovieContext": "Data Source=MvcMovie.db"
  }
}   

```C#
using RazorPagesMovie.Data;
using Microsoft.EntityFrameworkCore;

public void ConfigureServices(IServiceCollection services)
{
    services.AddRazorPages();

    services.AddDbContext<RazorPagesMovieContext>(options =>
        options.UseSqlite(Configuration.GetConnectionString("MovieContext")));
}
```   

dotnet aspnet-codegenerator razorpage -m Movie -dc RazorPagesMovieContext -udl -outDir Pages\Movies --referenceScriptLibraries   

dotnet aspnet-codegenerator razorpage -h   

dotnet ef migrations add InitialCreate    

                        <li class="nav-item">
                            <a class="nav-link text-dark" asp-area="" asp-page="/Index">Home</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link text-dark" asp-area="" asp-page="/Movies/Index">Movies</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link text-dark" asp-area="" asp-page="/Privacy">Privacy</a>
                        </li>   

DB Browser for SQLite <https://sqlitebrowser.org/>   

![DB Browser for SQLite](https://images.gitee.com/uploads/images/2020/0811/164951_c01f0cff_7799879.png)   

```C#
using System;
using System.ComponentModel.DataAnnotations;
using System.ComponentModel.DataAnnotations.Schema;

namespace RazorPagesMovie.Models
{
    public class Movie
    {
        public int ID { get; set; }
        public string Title { get; set; }

        [Display(Name = "Release Date")]
        [DataType(DataType.Date)]
        public DateTime ReleaseDate { get; set; }
        public string Genre { get; set; }

        [Column(TypeName = "decimal(18, 2)")]
        public decimal Price { get; set; }
    }
}
```


# MVC

# Web API

# SignalR

# gRPC

# EntityFramework(EF) Core

# asp dotnet core api