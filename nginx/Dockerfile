FROM alpine:3.2
RUN apk add --update nginx && rm -rf /var/cache/apk/*
RUN mkdir -p /tmp/nginx/client-body

COPY nginx.conf /etc/nginx/nginx.conf
COPY default.conf /etc/nginx/conf.d/default.conf

COPY ssl/cert.pem /etc/nginx/ssl/cert.pem
COPY ssl/selfsigned.pem /etc/nginx/ssl/selfsigned.pem

CMD ["nginx", "-g", "daemon off;"]
