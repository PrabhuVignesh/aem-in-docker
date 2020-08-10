# Using 'ubuntu' as the base image here
FROM ubuntu

# setting the working directory
WORKDIR /opt/aem

# Copy the license file
COPY license.properties .

# Copy Quickstart jar file
COPY cq-quickstart-6.5.0.jar cq-quickstart.jar

# Install Java
RUN apt-get update && \
    apt-get install -y curl && \
    apt-get install -y software-properties-common && \
    add-apt-repository ppa:openjdk-r/ppa && \
    apt-get update && \
    apt-get install -y openjdk-8-jdk

# Unack the Jar file
RUN java -jar cq-quickstart.jar -unpack
