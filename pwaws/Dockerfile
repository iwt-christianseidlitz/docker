FROM amazon/aws-cli

# default dotnet and powershell install
RUN curl -sSL https://dot.net/v1/dotnet-install.sh | bash /dev/stdin \
    && /root/.dotnet/dotnet tool install --global PowerShell

# export PATH=/root/.dotnet:/root/.dotnet/tools:$PATH
ENV PATH="/root/.dotnet:/root/.dotnet/tools:${PATH}"

# DOTNET_ROOT needs to be set
# export DOTNET_ROOT=$(dirname $(realpath $(which dotnet)))
ENV DOTNET_ROOT="/root/.dotnet"

# could use pwsh from here
# SHELL ["pwsh", "-command"]

ENTRYPOINT ["pwsh"]
