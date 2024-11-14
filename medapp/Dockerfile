# Use the official NGINX image as the base image
FROM nginx:latest

# Copy custom NGINX config if needed (optional)
# COPY nginx.conf /etc/nginx/nginx.conf

# Create a wrapper script
RUN echo '#!/bin/sh\n\n\
# Add any pre-run setup or environment variables here\n\
echo "Starting NGINX..."\n\
nginx -g "daemon off;"' > /usr/local/bin/start-nginx && \
    chmod +x /usr/local/bin/start-nginx

# Use the wrapper script as the container's entrypoint
ENTRYPOINT ["/usr/local/bin/start-nginx"]

# Expose the default NGINX port
EXPOSE 80
