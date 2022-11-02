# k81
Kubernetes for the Absolute Beginners - Hands-on (udemy.com)

===================================================
https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-CC0103EN-SkillsNetwork/labs/module-3-lab-1/index.md.html
https://raw.githubusercontent.com/IBM/MAX-Object-Detector/master/max-object-detector.yaml


How to create and deploy one service.
$ ibmcloud ks cluster config --cluster <clusterID>
How to copy from online repo
curl <Online file> > max-object-detector.yaml
$ kubectl apply -f max-object-detector.yaml
$ ibmcloud cs workers --cluster cd96ri1f05600fl9tdng
$ kubectl get pods
$ ibmcloud cs workers --cluster cd96ri1f05600fl9tdng
$ kubectl describe service max-object-detector | grep NodePort
===================================================
My Linux machine- 
Folder- /home/owner/kubernetes/services-deployments
kubectl apply -f maxobject-detector.yaml  myapp.yaml
Result-
http://159.122.183.222:30004/
http://159.122.183.222:30005/app/
$ kubectl get pods
$ kubectl get svc
NAME                  TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
kubernetes            ClusterIP   172.21.0.1       <none>        443/TCP          145m
max-object-detector   NodePort    172.21.108.244   <none>        5000:30005/TCP   17m
myapp-service         NodePort    172.21.14.193    <none>        80:30004/TCP     18m
$ curl http://172.21.108.244:5000/app/
$ curl http://172.21.14.193:80/app/
