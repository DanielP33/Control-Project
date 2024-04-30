FROM httpd:latest

# Copy SSL certificate and key to the container
COPY server.crt /usr/local/apache2/conf/server.crt
COPY server.key /usr/local/apache2/conf/server.key

# Enable SSL module and include SSL configuration
RUN sed -i \
        -e 's/^#\(Include .*httpd-ssl.conf\)/\1/' \
        -e 's/^#\(LoadModule .*mod_ssl.so\)/\1/' \
        -e 's/^#\(LoadModule .*mod_socache_shmcb.so\)/\1/' \
        /usr/local/apache2/conf/httpd.conf

# Generate your keys using this
# "openssl genrsa -out server.key 2048"
# "openssl req -new -key server.key -out server.csr"
# "openssl x509 -req -days 365 -in server.csr -signkey server.key -out server.crt"
# You should have server.crt / server.csr and server.key


# Then build your image and run it
# docker build -t my-apache-image .
# docker run -d -p 443:443 my-apache-image
# HTTPS Should be working now

# In case you're having problems your file structure should look like this:
# [root@RedHat apache]# ls
# Dockerfile  server.crt  server.csr  server.key

