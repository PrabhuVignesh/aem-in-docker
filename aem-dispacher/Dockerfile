# Using the apache base Image
FROM httpd:2.4

# Setting the current working directory
WORKDIR /usr/src/app

# Get the dispacher tar file and keepit inside 'dispacher' folder
ADD https://www.adobeaemcloud.com/content/companies/public/adobe/dispatcher/dispatcher/_jcr_content/top/download_8/file.res/dispatcher-apache2.4-linux-x86-64-4.2.3.tar.gz ./dispatcher/

# Extract the tar file and move it to Apache Modules folder with name mod_dispacher.so
RUN tar -xzvf ./dispatcher/dispatcher-apache2.4-linux-x86-64-4.2.3.tar.gz -C ./dispatcher && \
    cp ./dispatcher/dispatcher-apache2.4-4.2.3.so /usr/local/apache2/modules/mod_dispatcher.so

# Copy the dispacher.any file in to the Image in the below path
COPY dispatcher.any /usr/local/apache2/conf/dispatcher.any

# Copy the apache configuration file in the Image and paste it into the apache configuration path as mentioned below
COPY httpd.conf /usr/local/apache2/conf/httpd.conf
