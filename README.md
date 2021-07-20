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

![image](https://user-images.githubusercontent.com/87436052/126146250-911b55ec-53bf-458c-b549-ce64c2da9973.png)

![image](https://user-images.githubusercontent.com/87436052/126146404-b96ef533-0eef-48ee-afc8-204c31fe795c.png)

Solution 9:

kubectl create -f "C:\Yaml-Files\create-finance-pod.yaml"

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126275804-223bae65-7d49-4d3d-9696-84657a36e131.png)

kubectl get pods --namespace finance-zahi

![image](https://user-images.githubusercontent.com/87436052/126275837-60bd69b0-3932-40cc-9320-c9d7fe61007c.png)

Solution 10: 

(file Also Upload To Git AS: "Persistent Volume.yaml" ) https://github.com/ZahiCohen/JB/blob/main/Persistent%20Volume.yaml

kubectl create -f "C:\Users\zahi_c\Desktop\Persistent Volume.yaml"

![image](https://user-images.githubusercontent.com/87436052/126148054-cff72767-0f43-4088-b087-b48338d6a04b.png)

Solution 11:

kubectl create -f "C:\Users\zahi_c\Desktop\Pod-Empty-Dir.yaml"

yaml file : https://github.com/ZahiCohen/JB/blob/main/Pod-Empty-Dir.yaml

![image](https://user-images.githubusercontent.com/87436052/126150894-8e31eed7-cb17-43e4-8482-a5eac319df74.png)

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126151003-4a7c055d-165c-47a3-9f19-bd43d725f672.png)

Solution 12:

yaml file https://github.com/ZahiCohen/JB/blob/main/Create%20a%20PersistentVolume.yaml

kubectl create -f "C:\Users\zahi_c\Desktop\New folder\Create a PersistentVolume.yaml"

kubectl get pv pv-1

![image](https://user-images.githubusercontent.com/87436052/126155929-c8fc49d9-d4d6-452a-a35d-1a2c5d914bb0.png)

Create Claim : yaml : https://github.com/ZahiCohen/JB/blob/main/claim%20PersistentVolume.yaml

kubectl create -f "C:\Users\zahi_c\Desktop\New folder\claim PersistentVolume.yaml"

![image](https://user-images.githubusercontent.com/87436052/126156240-60591d27-b709-406e-ae16-447af38e7360.png)

Create Pod:

yaml : https://github.com/ZahiCohen/JB/blob/main/create%20pod%20with%20pv.yaml

kubectl create -f "C:\Users\zahi_c\Desktop\New folder\create pod with pv.yaml"

![image](https://user-images.githubusercontent.com/87436052/126158262-01d83e45-849c-45c7-a8ec-9c9b596982bc.png)

Solution 13:

kubectl create -f "C:\Users\zahi_c\Desktop\New folder\deploy-nginx-1.16.yaml"

yaml: https://github.com/ZahiCohen/JB/blob/main/deploy-nginx-1.16.yaml

![image](https://user-images.githubusercontent.com/87436052/126162563-120911fd-3269-465e-970b-3d904075db25.png)




















