# proxy/Dockerfile
FROM nginx:alpine

# Copy the Nginx configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Copy the HTML content to the default Nginx directory
COPY site /usr/share/nginx/html

RUN timestamp=$(date +'%Y-%m-%d %H:%M:%S') && echo "Current timestamp: $timestamp"