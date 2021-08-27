FROM node:16-alpine
RUN apk --no-cache add git
RUN git clone https://github.com/t2t2/obs-tablet-remote
WORKDIR /obs-tablet-remote
RUN npm i && npm run build
EXPOSE 5000
ENTRYPOINT [ "npm", "run", "start" ]
LABEL org.opencontainers.image.source="https://github.com/t2t2/obs-tablet-remote"