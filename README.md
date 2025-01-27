# Lesson 6 - Artifact-Repository-Manager-with-Nexus
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

## Configuring, Building and, Publishing artifacts from Gradle / Maven
### Maven-based Java project _java-maven-app_
- [x] Maven-based Java project `pom.xml` configuration file (artifact (groupID, artifactID, version), plugin `maven-deploy-plugin`, snapshotRepository url)
- [x] Maven configuration file `.m2/settings.xml` for id, username and password
- [x] Built artifact JAR file via `mvn package` command
- [x] Published JAR file via `mvn deploy` command

### Gradle-based Java project _java-app_
- [x] Gradle-based Java project `build.gradle` configuration file (artifact location, file type, targeted repository url, allowInsecureProtocol, credentials)
- [x] Gradle configuration file `settings.gradle` for project name
- [x] Gradle configuration file `gradle.properties` username / password
- [x] Built JAR fil via `gradle build` command
- [x] Published JAR file via `gradle publish` command
      
## API
- [x] Identified location APIs available on Nexus at `http://x.x.x.x:8081/#admin/system/api`

## Blob configuration
- [x] Created Blob of file type named `mystore`
- [x] `mystore` is not associated to a repository because association is permanent.  No repo to configure at this time

## Cleanup policies and task
- [x] Created `maven` cleanup policy as soft delete job, find .* (all), preview to repo `maven-snapshots` identified two (2) artifacts to soft delete.
- [x] Applied `maven` cleanup policy to reposititory `maven-snapshots`
- [x] Task `Cleanup service` deleted.
- [x] Task `compact-maven` created as permanent deletion of artifacts
- [x] Task `compact-maven` deleted for badge certification at TWN 
