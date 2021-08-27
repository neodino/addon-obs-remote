FROM node:16-alpine
RUN apk --no-cache add git
RUN git clone https://github.com/t2t2/obs-tablet-remote
WORKDIR /obs-tablet-remote
RUN npm i && npm run build
RUN npm install -g http-server
EXPOSE 5001
WORKDIR /obs-tablet-remote/dist/
ENTRYPOINT [ "http-server", "-c-1", "-p", "5001" ]
LABEL org.opencontainers.image.source="https://github.com/t2t2/obs-tablet-remote"