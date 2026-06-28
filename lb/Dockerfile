FROM nginx:alpine

# Remove default nginx config
RUN rm /etc/nginx/conf.d/default.conf

# Copy load balancer config
COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80
