FROM node:16-alpine
RUN apk --no-cache add git
RUN git clone https://github.com/Niek/obs-web 
WORKDIR /obs-web 
RUN npm i && npm run build
EXPOSE 5000
ENTRYPOINT [ "npm", "run", "start" ]
LABEL org.opencontainers.image.source="https://github.com/Niek/obs-web"