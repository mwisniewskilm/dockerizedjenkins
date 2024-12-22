# Dockerized jenkins configration


- path to java: /usr/lib/jvm/java-17-openjdk-amd64/bin/java
- run `docker logs jenkins | less` to get unlock password
- generate pair of `ssh-keys ssh-keygen -t rsa -f jenkins_agent`
- add public key to docker-compose
- you can build image with `docker build -t custom-jenkins-agent ./.docker/custom-jenkins-agent/`
- you can access machine with `docker exec agent bash`