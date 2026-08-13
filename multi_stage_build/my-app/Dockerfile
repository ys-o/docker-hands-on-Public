#@single-stage
# FROM nginx:1.27-alpine

# RUN apk add --no-cache nodejs npm
# RUN npm install -g npm@11.19.0

# WORKDIR /app

# COPY package*.json ./
# RUN npm ci

# COPY . .
# RUN npm run build

# RUN mv ./build/* /usr/share/nginx/html





#@multi-stage
FROM node:latest AS build-stage

RUN npm install -g npm@11.19.0

WORKDIR /app

COPY package*.json ./
RUN npm ci

COPY . .
RUN npm run build


FROM nginx:1.27-alpine

COPY --from=build-stage /app/build /usr/share/nginx/html