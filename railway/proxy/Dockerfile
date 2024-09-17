# proxy/Dockerfile
FROM nginx:1-alpine

# Copy the Nginx configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Expose port 80
EXPOSE 80

# Set the entrypoint
ENTRYPOINT ["nginx", "-g", "daemon off;"]