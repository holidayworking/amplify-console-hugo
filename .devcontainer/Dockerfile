FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:0-16-bullseye

RUN HUGO_URL=https://github.com/gohugoio/hugo/releases/download/v0.90.1/hugo_0.90.1_Linux-64bit.tar.gz \
  && curl --silent --show-error --location --fail --retry 3 --output /tmp/hugo.tar.gz $HUGO_URL \
  && tar -xz -C /tmp -f /tmp/hugo.tar.gz \
  && mv /tmp/hugo /usr/bin/hugo \
  && rm /tmp/hugo.tar.gz

EXPOSE 1313

USER node
