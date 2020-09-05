FROM jenkins/jenkins

USER root

# DIND(docker in docker)를 위해 docker 안에서 docker를 설치 
COPY docker_install.sh /docker_install.sh 
RUN chmod +x /docker_install.sh 
RUN /docker_install.sh 

# docker-compose
RUN ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
# RUN chmod +x /usr/local/bin/docker-compose

RUN usermod -aG docker jenkins 
