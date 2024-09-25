# proxy/Dockerfile
FROM nginx:1-alpine

# Copy the Nginx configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Set the entrypoint
ENTRYPOINT ["nginx", "-g", "daemon off;"]