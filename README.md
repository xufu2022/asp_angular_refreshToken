# asp_angular_refreshToken

```powershell
## dotnet --list-sdks
## dotnet --list-runtimes
dotnet new list

dotnet new sln --name JwtRefreshToken
dotnet new globaljson --sdk-version 7.0.100 --force
dotnet new webapi -o 'src\JwtRefreshToken.Server' -f net7.0
cd src\JwtRefreshToken.Server
dotnet add package Microsoft.EntityFrameworkCore.Design --version 7.0.0
dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 7.0.0
dotnet add package Microsoft.AspNetCore.Authentication.JwtBearer
dotnet build
dotnet ef migrations add InitialUserData
## dotnet ef database drop --force
dotnet ef database update
```