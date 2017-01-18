CI for UIP
==========

### In docker daemon

    $ docker run --name uip-ci -p 9102:8080 -p 50005:50000 -d propersoft/uip-ci
    $ docker exec -ti uip-ci bash

### In docker container

    # svn info https://{nexus_url}/svn/CodeManagement-all/trunk

Input `p` as `permanently` save server certificate

### In Jenkins

- Install git plugin manually and restart Jenkins
- Setup USER_SVN/PWD_SVN/USER_NEXUS/PWD_NEXUS/URL_NEXUS as environment variables in Jenkins instance

### In Jenkins Job

- Set git repository (https://gitlab.com/propersoft/pack-uip.git) and gitlab credentials
- Setup build steps and others
