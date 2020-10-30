FROM debian:buster-slim
ENV DENO_VERSION=1.5.0
RUN apt-get update \
    && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
        curl \
        unzip \
        ca-certificates \
    && apt-get -qq clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN curl -fsSL https://deno.land/x/install/install.sh | sh -s v${DENO_VERSION}
RUN echo 'export PATH="$HOME/.deno/bin:$PATH"' >> ~/.bashrc