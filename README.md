# WH-Task-1

> You will need to have pre-installed kubectl and Minikube.

The following are to be created in a kubernetes cluster:
- deployment, svc, hpa, pdb, secret, service account, role, rolebinding


## To begin run the following command which will start Minikube
	> minikube start

## Deploying to Kubernetes service
	> kubectl apply -f deployment.yaml,hpa.yaml,pdb.yaml,api-key-secret.yaml,service-account.yaml,role.yaml,rb.yaml

## Verify that everything is created successfully
	> kubectl get deploy,svc,hpa,pdb,secret,sa,role,rolebinding

#### Or use the Minikube dashboard which can be accessed via
	> minikube dashboard

## To access the Apache HTTP default page through your browser, execute the following:
	> kubectl port-forward svc/svc-httpd 31000:8000 &

## Go to your browser and open
	> 127.0.0.1:31000

You should see "It works!".

## To kill the process execute
	> pkill kubectl
