FROM alpine:3.20

LABEL org.opencontainers.image.source="https://github.com/Captnlink/adr-tools"
LABEL org.opencontainers.image.description="Command-line tools for working with Architecture Decision Records"
LABEL org.opencontainers.image.licenses="GPL-3.0-or-later"
LABEL org.opencontainers.image.version="1.0.0"

RUN apk update && apk add --no-cache \
   bash \
   bash-completion \
   && mkdir -p /etc/bash_completion.d

COPY src /adr-src
COPY autocomplete/adr /etc/bash_completion.d/001_adr

ENV PATH="$PATH:/adr-src/"

ENTRYPOINT [ "/adr-src/adr" ]
