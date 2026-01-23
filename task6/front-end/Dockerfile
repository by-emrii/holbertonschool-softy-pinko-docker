# Use the latest nginx image
FROM nginx:latest

# copy softy pinko files to /var/www...
COPY softy-pinko-front-end /var/www/html/softy-pinko-front-end

# copy nginx config file to docker img /etc/...
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf 