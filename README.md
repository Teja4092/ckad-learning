# ckad-learning

# Commands

kubectl get all
kubectl get pods
kubectl get ns
kubectl get replicasets
kubectl get deployments
kuectl get pods -n <namespace>
kubectl scale --replicas=6 -f rc-srt.yml
kubectl get deployments nginx-deployment -o yaml
kubectl config set-context $(kubectl config current-context) --namespace=dev
kubectl scale deployment nginx --replicas=4
kubectl create deployment nginx --image=nginx --replicas=4
kubectl expose pod redis --port=6379 --name redis-service --dry-run=client -o yaml
kubectl create svc nodeport myapp --tcp=80:80 --node-port=30080 --dry-run=client -o yaml 
kubectl create svc nodeport myapp --tcp=80:80 --node-port=30080

--dry-run: By default, as soon as the command is run, the resource will be created. 

If you simply want to test your command, use the --dry-run=client option. This will not create the resource. Instead, tell you whether the resource can be created and if your command is right.

-o yaml: This will output the resource definition in YAML format on the screen.
