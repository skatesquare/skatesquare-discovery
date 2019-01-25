# SkateSquare Discovery
Spring Eureka discovery server for all SkateSquare microservices.

## Building docker images
The Gradle plugin [com.zoltu.git-versioning](https://plugins.gradle.org/plugin/com.zoltu.git-versioning) is used to update the patch version of this project for every commit.
The Gradle plugin [com.palantir.docker](https://plugins.gradle.org/plugin/com.palantir.docker) is used to configure some Tasks to build, tag and push docker images to Docker Hub.

When you want to create and push a new version to Docker Hub simply run the following commands.
```
(Linux/macOS/bash)
$ ./gradlew build docker dockerTag 
$ ./gradlew dockerPush

(Windows/cmd)
$ gradlew.bat build docker dockerTag
$ gradlew.bat dockerPush
```