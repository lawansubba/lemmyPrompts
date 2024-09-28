# proxy/Dockerfile
FROM nginx:alpine

# Copy the Nginx configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Copy the HTML content to the default Nginx directory
COPY index.html /usr/share/nginx/html/index.html

RUN timestamp=$(date +'%Y-%m-%d %H:%M:%S') && echo "Current timestamp: $timestamp"

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]