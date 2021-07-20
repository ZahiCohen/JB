# JB
מטלה מסכמת גון ברייס

המטלה נעשתה על מיניקיוב בווינדוס 10
יש להוריד את קבצי הימל לתקייה ולהריץ בהתאם לנתיב הנכון

Solution 1 : 

kubectl create -f "C:\Yaml-Files\nginx-pod-zahi.yaml"

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126272697-2c52f137-5329-46fa-9fb0-36481060127e.png)

Solution 2:

kubectl create -f "C:\Yaml-Files\messaging-pod.yaml"

kubectl get pods

kubectl get pods -l "tier=msg"

![image](https://user-images.githubusercontent.com/87436052/126273346-d075ee12-310f-4500-89d8-8393a7601d67.png)

Solution 3:

kubectl create namespace apx-x998-zahi

![image](https://user-images.githubusercontent.com/87436052/126072299-ac068b11-5c1d-484b-8df0-f753f3fb3eaf.png)

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126072318-edcb2d30-54f7-469a-9f7d-418764f35531.png)

Solution 4:

kubectl get nodes -o jsonpath='/tmp/nodes-zahi'

![image](https://user-images.githubusercontent.com/87436052/126060293-758bcbf2-3d9a-486d-a0cc-bc3d8afd172f.png)

Solution 5:

kubectl create -f "C:\Yaml-Files\messaging-service.yaml"

kubectl get svc

![image](https://user-images.githubusercontent.com/87436052/126273857-dcb677ef-5109-42c0-8717-e221c5684ba9.png)

Solution 7: 

kubectl create -f "C:\Yaml-Files\hr-web-app-deploy.yaml"

kubectl get replicaset

![image](https://user-images.githubusercontent.com/87436052/126274700-41bcfb87-c0f1-4e47-98a5-62c741a64708.png)

Solution 8: 

1. How to find master node:  
 
kubectl get nodes

![image](https://user-images.githubusercontent.com/87436052/126146046-5bdfb40b-4c5c-4a06-8478-8e1526b69200.png)

2. run on master node:

kubectl run --restart=Never --image=busybox static-busybox -o yaml --command -- sleep 1000 > /etc/kubernetes/manifests/static-busybox.yaml

run on minikube:

kubectl run --restart=Never --image=busybox static-busybox -o yaml --command -- sleep 1000

![image](https://user-images.githubusercontent.com/87436052/126146250-911b55ec-53bf-458c-b549-ce64c2da9973.png)

![image](https://user-images.githubusercontent.com/87436052/126146404-b96ef533-0eef-48ee-afc8-204c31fe795c.png)

Solution 9:

kubectl create -f "C:\Yaml-Files\create-finance-pod.yaml"

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126275804-223bae65-7d49-4d3d-9696-84657a36e131.png)

kubectl get pods --namespace finance-zahi

![image](https://user-images.githubusercontent.com/87436052/126275837-60bd69b0-3932-40cc-9320-c9d7fe61007c.png)

Solution 10: 

kubectl create -f "C:\Yaml-Files\persisten-vol.yaml"

kubectl get pv

![image](https://user-images.githubusercontent.com/87436052/126276667-8dde514b-e61f-4382-b566-28c8111597c3.png)

Solution 11:

kubectl create -f "C:\Yaml-Files\redis-storage-zahi-pod.yaml"

![image](https://user-images.githubusercontent.com/87436052/126277072-e2f0d87a-19ff-49f9-8798-9fd79e5ae3ad.png)

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126277135-f52c63dc-33ee-43e8-b78e-76af78b8473e.png)

Solution 12:

kubectl create -f "C:\Yaml-Files\nginx-pod-attach.yaml"

kubectl get pvc pv-1

kubectl get pods use-pv-zahi

![image](https://user-images.githubusercontent.com/87436052/126277986-64ea7098-ab4e-4885-a4e1-3d31771ed067.png)

Solution 13:

kubectl create -f "C:\Yaml-Files\nginx-deploy.yaml"

kubectl get deployments nginx-deploy

kubectl set image deployments nginx-deploy nginx=nginx:1.17 --record

![image](https://user-images.githubusercontent.com/87436052/126278469-e99517bb-8ec9-47e3-8bc4-9c27d6427a3b.png)

kubectl describe deployments nginx-deploy

![image](https://user-images.githubusercontent.com/87436052/126278779-aeb8a90e-4013-4e91-9728-9a3c4db5c1a1.png)

Solution 14:

kubectl create -f "C:\Yaml-Files\nginx-resolver.yaml"

kubectl get svc nginx-resolver-service

kubectl get pods nginx-resolver

kubectl run test-nslookup --image=busybox:1.28 -- nslookup nginx-resolver-service

kubectl logs test-nslookup

![image](https://user-images.githubusercontent.com/87436052/126282587-a04fcaff-1cf9-4654-a85b-18bbdf083dea.png)


Solution 15: skip

Solution 16:

kubectl create -f "C:\Yaml-Files\multi-pod.yaml"

kubectl get pods

kubectl describe pods multi-pod

![image](https://user-images.githubusercontent.com/87436052/126284734-d5f17ca0-8cf2-4f01-a5d0-2426ee811f01.png)


![image](https://user-images.githubusercontent.com/87436052/126284930-55688e2a-c632-4335-bdfb-7fd52c20e2fe.png)


Pod Design Answres:

1. 






















