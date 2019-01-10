FROM alpine:latest

LABEL version="1.0.0"
LABEL repository="http://github.com/mint-lang/actions"
LABEL homepage="http://github.com/mint-lang/actions/cli"
LABEL maintainer="Mint"

LABEL "com.github.actions.name"="Mint CLI"
LABEL "com.github.actions.description"="Wraps the Mint CLI to enable common commands"
LABEL "com.github.actions.icon"="git-commit"
LABEL "com.github.actions.color"="gray-dark"

RUN wget -O mint https://github.com/mint-lang/mint/releases/download/0.3.1/mint-0.3.1-linux
RUN chmod +x mint

COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
