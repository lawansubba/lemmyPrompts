# proxy/Dockerfile
FROM nginx:1-alpine

# Copy the Nginx configuration file
COPY nginx.conf /etc/nginx/nginx.conf

RUN timestamp=$(date +'%Y-%m-%d %H:%M:%S') && echo "Current timestamp: $timestamp"

CMD ["nginx", "-g", "daemon off;"]