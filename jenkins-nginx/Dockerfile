#
# Nginx Dockerfile
#
# https://github.com/dockerfile/nginx
#

# Pull base image.
#FROM ubuntu:18.04 as base
FROM ubuntu:18.04

# Install Nginx.
RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:nginx/stable
RUN apt-get install -y nginx
RUN rm -rf /var/lib/apt/lists/* 
  #&& \
  #echo "\ndaemon off;" >> /etc/nginx/nginx.conf && \
RUN chown -R www-data:www-data /var/lib/nginx

# Cleanup the default NGINX configuration file
#RUN rm /etc/nginx/conf.d/default.conf

# Add our configuration files
COPY conf/jenkins.conf /etc/nginx/conf.d/jenkins.conf
COPY conf/nginx.conf /etc/nginx/nginx.conf

# Define mountable directories.
#VOLUME ["/etc/nginx/sites-enabled", "/etc/nginx/certs", "/etc/nginx/conf.d", "/var/log/nginx", "/var/www/html"]

# Define working directory.
#WORKDIR /etc/nginx

# Define default command.
CMD ["nginx"]

# Expose ports.
EXPOSE 80
#EXPOSE 443

