FROM nginx:alpine
# Overwrite the default Nginx config with our reverse proxy config
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY index.html /usr/share/nginx/html/
EXPOSE 80
