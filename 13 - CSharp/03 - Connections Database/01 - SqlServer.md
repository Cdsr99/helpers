## Connection with SQL Server

1) Iniciate the services:

```shell

builder.Services.
    AddDbContext<RodBooksDbContext>(option => option
        .UseLazyLoadingProxies().UseSqlServer(builder.Configuration.GetConnectionString("Connection")));
```

2) DbConnection
```shell
public class RodBooksDbContext : DbContext 
{
        public RodBooksDbContext(DbContextOptions opts) : base(opts)
    {
        
    }
}
```
