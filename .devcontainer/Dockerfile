FROM mcr.microsoft.com/devcontainers/base:alpine

RUN apk update && apk add --no-cache \
    zsh \
    curl \
    git \
    icu-libs \
    krb5-libs \
    libgcc \
    libintl \
    libssl3 \
    libstdc++ \
    zlib

RUN sed -i 's/bin\/ash/bin\/zsh/g' /etc/passwd

RUN curl -sSL https://dot.net/v1/dotnet-install.sh | bash /dev/stdin --version 10.0 --install-dir /usr/local/bin

ENV DOTNET_ROOT=/usr/local/bin
ENV PATH=$PATH:$DOTNET_ROOT