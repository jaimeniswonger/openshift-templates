### Create zipkin application

	oc process -f zipkin/zipkin-template.yml | oc create -f - -n itweb-infra
	
### Start Build

	oc start-build itweb-zipkin -n itweb-infr
	
#### Note: The deployment will start automatically after the build is complete.		