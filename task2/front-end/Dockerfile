# Use the latest nginx image as the base
FROM nginx:latest

# Copy the cloned front-end files into the container
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy our custom config to the Nginx configuration directory
# This overwrites the default Nginx welcome page config
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
