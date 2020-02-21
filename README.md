# algorithms
Codebase for Princeton Algorithm course

# Java Docker Instance
https://hub.docker.com/_/openjdk

Using Docker as runtime and build time:

Example Dockerfile: 

```
FROM openjdk:7
COPY . /usr/src/myapp
WORKDIR /usr/src/myapp
RUN javac Main.java
CMD ["java", "Main"]
```
And build / run:

```
$ docker build -t my-java-app .
$ docker run -it --rm --name my-running-app my-java-app
```
