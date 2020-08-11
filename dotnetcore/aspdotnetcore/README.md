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

```C#
public class IndexModel : PageModel
{
    private readonly RazorPagesMovie.Data.RazorPagesMovieContext _context;

    public IndexModel(RazorPagesMovie.Data.RazorPagesMovieContext context)
    {
        _context = context;
    }

    public IList<Movie> Movie { get; set; }
    [BindProperty(SupportsGet = true)]
    public string SearchString { get; set; }
    // Requires using Microsoft.AspNetCore.Mvc.Rendering;
    public SelectList Genres { get; set; }
    [BindProperty(SupportsGet = true)]
    public string MovieGenre { get; set; }
```   

```C#
public async Task OnGetAsync()
{
    // Use LINQ to get list of genres.
    IQueryable<string> genreQuery = from m in _context.Movie
                                    orderby m.Genre
                                    select m.Genre;

    var movies = from m in _context.Movie
                 select m;

    if (!string.IsNullOrEmpty(SearchString))
    {
        movies = movies.Where(s => s.Title.Contains(SearchString));
    }

    if (!string.IsNullOrEmpty(MovieGenre))
    {
        movies = movies.Where(x => x.Genre == MovieGenre);
    }
    Genres = new SelectList(await genreQuery.Distinct().ToListAsync());
    Movie = await movies.ToListAsync();
}
```

```html
@page   
@model RazorPagesMovie.Pages.Movies.IndexModel

@{   
    ViewData["Title"] = "Index";
}   

<h1>Index</h1>

<p>   
    <a asp-page="Create">Create New</a>
</p>   

<form>   
    <p>   
        <select asp-for="MovieGenre" asp-items="Model.Genres">   
            <option value="">All</option>   
        </select>   
        Title: <input type="text" asp-for="SearchString" />   
        <input type="submit" value="Filter" />   
    </p>   
</form>   

<table class="table">   
    @*Markup removed for brevity.*@      
```


# MVC   

dotnet new mvc -o MvcMovie   
code -r MvcMovie   

dotnet dev-certs https --trust

```C#
using Microsoft.AspNetCore.Mvc;
using System.Text.Encodings.Web;

namespace MvcMovie.Controllers
{
    public class HelloWorldController : Controller
    {
        // 
        // GET: /HelloWorld/

        public string Index()
        {
            return "This is my default action...";
        }

        // 
        // GET: /HelloWorld/Welcome/ 

        public string Welcome()
        {
            return "This is the Welcome action method...";
        }
    }
}
```

<https://localhost:5001/Helloworld/welcome>   

```C#
// GET: /HelloWorld/Welcome/ 
// Requires using System.Text.Encodings.Web;
public string Welcome(string name, int numTimes = 1)
{
    return HtmlEncoder.Default.Encode($"Hello {name}, NumTimes is: {numTimes}");
}
```

<https://localhost:{PORT}/HelloWorld/Welcome?name=Rick&numtimes=4>   

```C#
public string Welcome(string name, int ID = 1)
{
    return HtmlEncoder.Default.Encode($"Hello {name}, ID: {ID}");
}
```

<https://localhost:{PORT}/HelloWorld/Welcome/3?name=Rick>   

```C#
app.UseEndpoints(endpoints =>
{
    endpoints.MapControllerRoute(
        name: "default",
        pattern: "{controller=Home}/{action=Index}/{id?}");
});
```


# Web API

dotnet new webapi -o TodoApi   
cd TodoApi   
dotnet add package Microsoft.EntityFrameworkCore.SqlServer   
dotnet add package Microsoft.EntityFrameworkCore.InMemory   
code -r ../TodoApi   

<https://localhost:5001/WeatherForecast>   



# SignalR

dotnet new webapp -o SignalRChat    
code -r SignalRChat   

dotnet tool install -g Microsoft.Web.LibraryManager.Cli    

libman install @microsoft/signalr@latest -p unpkg -d wwwroot/js/signalr --files dist/browser/signalr.js --files dist/browser/signalr.min.js   

dotnet watch run -p SignalRChat.csproj   



# gRPC   

dotnet new grpc -o GrpcGreeter   
code -r GrpcGreeter   

  
# EntityFramework(EF) Core

# asp dotnet core api