### Create build configuration

	oc create -f zipkin-buildconfig.yml -n infra-poc


### Create zipkin application

	oc create -f zipkin-application.yml -n infra-poc 
	
### Start Build

	oc start-build itweb-zipkin -n infra-poc
	
#### Note: The deployment will start automatically after the build is complete.		