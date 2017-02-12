# tomcat-secret
Docker image extending form the official tomcat alpine image with docker secret functionality

Docker secrets are automatically replaced in any of the .xml files in the tomcat config directory.

This could be used to inject database passwords into JNDI configurations without baking them into the image or using unsecure environment variables.

The name of the secret is replaced in the same format as other tomcat properties e.g. ${docker.secret.name} will be replaced with the value of the docker secret docker.secret.name.