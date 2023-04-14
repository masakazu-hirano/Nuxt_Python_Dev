FROM node:18.16.0

ENV BW_CLIENTID '値'
ENV BW_CLIENTSECRET '値'

COPY . /usr/local/src
WORKDIR /usr/local/src/'アプリケーション名'

RUN apt-get update && apt-get install -y vim
RUN npm install npm@latest -g && npm install -g @bitwarden/cli \
  && npm install

RUN bw login --apikey

CMD ["npm", "run", "dev", "--", "-o"]
