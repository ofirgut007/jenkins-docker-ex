FROM evarga/jenkins-slave

MAINTAINER Lev Epshtein 

# Make sure the packages is up to date
RUN apt-get update
#RUN apt-get -y upgrade

# Install Subversion and Git
RUN apt-get -y install git subversion

# Install maven3
RUN apt-get install -y wget &&\
    cd /usr/local &&\
    wget http://www-eu.apache.org/dist/maven/maven-3/3.5.2/binaries/apache-maven-3.5.2-bin.tar.gz &&\
    tar xzf apache-maven-3.5.2-bin.tar.gz &&\
    rm apache-maven-3.5.2-bin.tar.gz &&\ 
    ln -s apache-maven-3.5.2 apache-maven &&\
    ln -s /usr/local/apache-maven/bin/mvn /bin/mvn
