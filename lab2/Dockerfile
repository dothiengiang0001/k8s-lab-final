# Dockerfile
FROM nginx:latest

# Copy Nginx configuration
COPY nginx.conf /etc/nginx/nginx.conf

# Copy HTML file
COPY source /usr/share/nginx/html

RUN chmod -R 777 /usr/share/nginx/html

# Set the default command to start Nginx
CMD ["nginx", "-g", "daemon off;"]
