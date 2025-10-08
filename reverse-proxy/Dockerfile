FROM nginx:stable-alpine

ARG BACKEND_URL=http://10.20.0.1:3000

COPY reverse-proxy.conf /etc/nginx/conf.d/reverse-proxy.conf

RUN sed -i "s|http://10.20.0.1:3000|${BACKEND_URL}|g" /etc/nginx/conf.d/reverse-proxy.conf

EXPOSE 443
