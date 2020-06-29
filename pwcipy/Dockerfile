FROM cimg/python:3.8-node

RUN sudo curl -sSL https://dot.net/v1/dotnet-install.sh | bash /dev/stdin \
    && sudo /home/circleci/.dotnet/dotnet tool install --global PowerShell

ENV PATH="/home/circleci/.dotnet:/home/circleci/.dotnet/tools:${PATH}"

ENV DOTNET_ROOT="/home/circleci/.dotnet"

ENTRYPOINT ["pwsh"]
