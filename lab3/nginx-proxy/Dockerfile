# Dockerfile
FROM nginx:latest

# Copy Nginx configuration
COPY nginx.conf /etc/nginx/nginx.conf

# Copy HTML files
COPY source /usr/share/nginx/html

# Expose port 80
EXPOSE 80

# Start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]

