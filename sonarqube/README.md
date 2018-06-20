# SONARQUBE NOTES

#### OWASP has not tagged there owasp/sonarqube image other than 'latest', so we are maintaining a tag of that image using the owasp-sonarqube imagestream.  It can be pushed to the OpenShift registry as follows: 

##### Pull the latest
`docker pull owasp/sonarqube:latest`

##### Tag it
`docker tag owasp/sonarqube registry.awsos2.americancentury.com/itweb-ci-cd/owasp-sonarqube:v1.0`

##### Docker login
##### Note: You must be logged in as admin (or user with system:admin rights) and have the registry trusted in your docker daemon
`docker login -u admin -p $(oc whoami -t) registry.awsos2.americancentury.com`  

##### Push the tag
`docker push registry.awsos2.americancentury.com/itweb-ci-cd/owasp-sonarqube:v1.0`

 