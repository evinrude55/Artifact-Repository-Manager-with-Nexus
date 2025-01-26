# Artifact-Repository-Manager-with-Nexus
***DevOps Techworld with nana***

## Project Description
***Demo Project***
 Run Nexus on Droplet and Publish Artifact to Nexus

***Technologies used***
 Nexus, DigitalOcean, Linux, Java, Gradle, Maven

## Create a Nexus cloud server
- [x] Installed and configured Nexus server from scratch on DigitalOcean
- [x] `ps aux | grep nexus` -> fetched pid and tcp port
- [x] opened relevant firewall rules
- [x] successfully connected to x.x.x.x:8081

## Security considerations for Nexus publications
- [x] created new User for publications of artifacts
- [x] created new role _nx-java_ (set of privileges)
- [x] granted new User with role _nx-java_

## Publishing artifacts from Maven

