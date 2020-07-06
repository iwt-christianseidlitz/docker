FROM vittel/pwnode

RUN apt-get update && apt-get install -y zip && dotnet tool update -g Amazon.Lambda.Tools \
    && curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install \
    && npm install -g aws-cdk \
    && npm install -g aws-cdk

ENTRYPOINT ["pwsh"]
