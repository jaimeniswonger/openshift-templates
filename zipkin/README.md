### To create Docker image (from this folder):

	docker build -t itweb-zipkin .

### To push Docker image to OpenShift

  1. Tag the image:
  
	docker tag itweb-zipkin registry.awsos1.americancentury.com/infra-poc/itweb-zipkin
		
  2. Login to Openshift as admin:
  
	oc login https://awsos1.americancentury.com:8443
  		
  3. Login to Registry:
  
	docker login -u admin -p $(oc whoami -t) registry.awsos1.americancentury.com
      	
  4. Push the image:
  
	docker push registry.awsos1.americancentury.com/infra-poc/itweb-zipkin       	

### To create zipkin application on Openshift

	oc create -f zipkin-template.yml -n infra-poc 