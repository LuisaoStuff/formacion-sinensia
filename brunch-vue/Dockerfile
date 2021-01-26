FROM node:lts-buster as nodebuild
COPY . /build
WORKDIR /build
RUN npm install -g brunch
RUN brunch build --production

FROM nginx
COPY --from=nodebuild /build/public/ /usr/share/nginx/html
ENTRYPOINT ["nginx", "-g", "daemon off;"]
