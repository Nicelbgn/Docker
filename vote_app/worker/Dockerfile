FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build-env

WORKDIR /app

COPY Worker.csproj .

RUN dotnet restore

COPY . .

RUN dotnet publish -c release -o out

FROM mcr.microsoft.com/dotnet/runtime:7.0

WORKDIR /app

COPY --from=build-env /app/out .

CMD ["dotnet", "Worker.dll"]
