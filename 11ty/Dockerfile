# Dockerfile for 11ty Framework

FROM node:lts-alpine

WORKDIR /app

RUN npm install -g @11ty/eleventy

EXPOSE 8080

ENTRYPOINT [ "npx", "eleventy" ]
