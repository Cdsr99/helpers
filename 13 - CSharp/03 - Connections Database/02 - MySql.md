## Connection with MySql

1) Iniciate the services:

```shell
var connectionString = builder.Configuration.GetConnectionString("Connection");
builder.Services.AddDbContext<RifasContext>(options =>
    options.UseMySql(connectionString, ServerVersion.AutoDetect(connectionString)));
```

2) DbConnection
```shell
public class RifasContext : DbContext
{
    public RifasContext(DbContextOptions options) : base(options)
    {

    }
}
```
