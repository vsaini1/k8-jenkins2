# k8s-jenkins1


kubectl create namespace jenkins

#kubectl get namespaces

kubectl apply -f jenkins-volume.yaml

kubectl apply -f jenkins-sa.yaml

kubectl create -f jenkins-deployment.yaml -n jenkins

#kubectl get deployments -n jenkins

kubectl create -f jenkins-service.yaml -n jenkins

#kubectl get services -n jenkins

Now we can access the Jenkins instance at hostIP:port 192.168.99.100:30104/

kubectl get pods -n jenkins

Once you locate the name of the pod, use it to access the pod’s logs.

$ kubectl logs <pod_name> -n jenkins
