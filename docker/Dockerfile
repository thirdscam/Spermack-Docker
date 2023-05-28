FROM node:19.1.0-alpine3.16

ARG APP_HOME=/home/node/app

WORKDIR ${APP_HOME}

# Bundle app source
RUN apk add git
RUN git clone https://github.com/AmmoniaM/Spermack.git .

# Clean up
RUN rm start.bat config.js README.md

RUN chmod +x start.sh
ENTRYPOINT [ "/bin/sh", "-c", "./start.sh" ]
