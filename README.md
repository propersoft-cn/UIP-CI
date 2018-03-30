CI for UIP
==========

### In docker daemon

    # Start uip-ci container
    $ docker run --name uip-ci -p 8080:8080 -p 50000:50000 -v /opt/jenkins/m2:/root/.m2 -v /opt/jenkins/jobs:/var/jenkins_home/jobs -d propersoft/uip-ci
    # Into container
    $ docker exec -ti uip-ci bash

### In docker container

    # svn info https://{nexus_url}/svn/CodeManagement-all/trunk

Press `p` as `permanently` save server certificate, input and store svn username & password

### In Jenkins

- Install git plugin manually and restart Jenkins
- Setup USER_SVN/PWD_SVN/USER_NEXUS/PWD_NEXUS/URL_NEXUS as environment variables in Jenkins instance

### In Jenkins Job

- Set git repository (https://gitlab.com/propersoft/pack-uip.git) and gitlab credentials
- Setup build steps and others

### Work Path

`/var/jenkins_home`
