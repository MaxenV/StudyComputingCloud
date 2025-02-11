# Stage 1
FROM scratch AS stage1
ADD alpine-minirootfs-3.19.1-x86_64.tar /

RUN apk add --no-cache --repository=http://dl-cdn.alpinelinux.org/alpine/edge/community nodejs npm

WORKDIR /app

COPY ./package.json ./
RUN npm install

COPY ./index.js ./

ARG VERSION
ENV VERSION=app.${VERSION:-noVersion}

EXPOSE 8080

CMD [ "npm", "start" ]


# # Stage 2 
# FROM nginx:latest 

# COPY --from=stage1 /app /usr/share/nginx/html
# EXPOSE 80

# HEALTHCHECK --interval=10s --timeout=1s \
#     CMD curl -f http://localhost:80/ || exit 1

# CMD ["nginx", "-g", "daemon off;"]