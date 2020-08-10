# Use the previously created aem-base-image
FROM aem-base-image

# Expose AEM author in port 4502
EXPOSE 4502

# Make the container start always in Author mode with Port 4502
ENTRYPOINT ["java", "-jar", "cq-quickstart.jar", "-Dsling.run.modes=author", "-p", "4502"]
