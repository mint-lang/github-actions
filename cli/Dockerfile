FROM alpine:latest

LABEL version="1.0.0"
LABEL repository="http://github.com/mint-lang/actions"
LABEL homepage="http://github.com/mint-lang/actions/cli"
LABEL maintainer="Mint"

LABEL "com.github.actions.name"="Mint CLI"
LABEL "com.github.actions.description"="Wraps the Mint CLI to enable common commands"
LABEL "com.github.actions.icon"="git-commit"
LABEL "com.github.actions.color"="gray-dark"

RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh file imagemagick

RUN wget -O mint https://bintray.com/mint-lang/mint/download_file?file_path=mint-latest-linux
RUN chmod +x mint

COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
