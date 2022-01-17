# build stage
FROM node:lts-alpine as build-stage
RUN npm i -g pnpm
RUN npm install -g typescript

WORKDIR /app
COPY . .

RUN pnpm install --recursive
RUN pnpm run build

# production stage
FROM nginx:stable-alpine as production-stage
COPY --from=build-stage /app/dist /usr/share/nginx/html
COPY --from=build-stage /app/config /etc/nginx/

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]