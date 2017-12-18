FROM openjdk:8

WORKDIR /

RUN wget https://github.com/DSpace/DSpace/releases/download/dspace-6.2/dspace-6.2-release.tar.gz && \
    tar xvfzp dspace-6.2-release.tar.gz

COPY local.cfg /dspace-6.2-release/dspace/config/local.cfg

RUN apt update && apt install -y maven && cd /dspace-6.2-release && mvn package

COPY copy-dspace /bin
RUN chmod 755 /bin/copy-dspace

CMD echo 'To copy the dspace code, run "docker-compose run dspace-build copy-dspace"'