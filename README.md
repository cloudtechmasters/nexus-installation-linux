# nexus-installation-linux

## Install Java:
    yum install java-1.8.0-openjdk-devel java-1.8.0-openjdk-devel –y
    cd /opt
## Download nexus tar file:
    wget https://sonatype-download.global.ssl.fastly.net/nexus/3/nexus-3.0.2-02-unix.tar.gz
## Extract tar file:
    tar xvzf nexus-3.0.2-02-unix.tar.gz
## Change name of Nexus file:
    mv nexus-3.0.2-02/ nexus
## Add nexus user: 
    useradd nexus
## Change owner ship for nexus file:
    chown -R nexus:nexus nexus
## Open /opt/nexus/bin/nexus.rc file and update data like as below:
    run_as_user="nexus"
## Link file:
    ln -s /opt/nexus/bin/nexus /etc/init.d/nexus
## Login to nexus user:
    su - nexus
## Start nexus:
    service nexus start
## Check status of nexus:
    service nexus status
## Now give our domain name in UI and check whether Nexus opened or not with https:
    http://100.26.240.37:8081/
## Nexus credentials
    username: admin
    Password: admin123
