# TO BUILD THE IMAGE 

docker build -t my-jenkins-docker .
docker run -d \
  -p 8080:8080 \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v jenkins_home:/var/jenkins_home \
  my-jenkins-docker
