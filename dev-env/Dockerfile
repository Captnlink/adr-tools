FROM alpine:3.20

RUN apk update && apk add --no-cache \
   bash \
   bash-completion \
   && mkdir -p /etc/bash_completion.d

COPY src /adr-src
COPY autocomplete/adr /etc/bash_completion.d/001_adr

ENV PATH="$PATH:/adr-src/"

ENTRYPOINT [ "/adr-src/adr" ]
