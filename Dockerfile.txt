FROM nginx:latest
COPY webapp /usr/share/nginx/html
EXPOSE 80