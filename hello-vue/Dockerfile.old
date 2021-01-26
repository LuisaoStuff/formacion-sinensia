FROM node:lts-buster as nodebuild
COPY . /build
WORKDIR /build
RUN npm run build

FROM nginx
COPY --from=nodebuild /build/dist/ /usr/share/nginx/html
ENTRYPOINT ["nginx", "-g", "daemon off;"]
