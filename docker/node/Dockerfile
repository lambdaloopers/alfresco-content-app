FROM library/node:9.0

ARG USER_ID=1000
ARG GROUP_ID=1000

RUN groupmod -g ${GROUP_ID:-1000} node \
  && usermod -u ${USER_ID:-1000} node

COPY . /home/nodejs
COPY ./docker/node/entrypoint.sh /entrypoint.sh

USER node

WORKDIR /home/nodejs

ENTRYPOINT ["/entrypoint.sh"]
