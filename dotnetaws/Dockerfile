FROM mcr.microsoft.com/dotnet/core/sdk:3.1

SHELL ["pwsh", "-command"]

RUN apt-get update && apt-get install -y zip && dotnet tool update -g Amazon.Lambda.Tools
RUN New-Item -ItemType Directory -Force -Path (Split-Path $profile -Parent); \
    Add-Content $profile '$env:PATH = "$($env:PATH):/root/.dotnet/tools"'

ENTRYPOINT ["pwsh"]
