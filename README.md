# JB
מטלה מסכמת גון ברייס

Solution 1 : 

kubectl run nginx-pod-zahi --image=nginx:latest --port=8080

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126072081-a24530b5-ae8f-4d1b-a7c2-557373c2a11b.png)

Solution 2:

kubectl run messaging --image=redis --labels="tier=msg"

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126072138-335c774a-e041-4bbc-b32f-e35e893098b2.png)

kubectl get pods -l "tier=msg"

![image](https://user-images.githubusercontent.com/87436052/126072226-1f918e91-b3f8-4a20-b295-ca31e6198459.png)

Solution 3:

kubectl create namespace apx-x998-zahi

![image](https://user-images.githubusercontent.com/87436052/126072299-ac068b11-5c1d-484b-8df0-f753f3fb3eaf.png)

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126072318-edcb2d30-54f7-469a-9f7d-418764f35531.png)

Solution 4:

kubectl get nodes -o jsonpath='/tmp/nodes-zahi'

![image](https://user-images.githubusercontent.com/87436052/126060293-758bcbf2-3d9a-486d-a0cc-bc3d8afd172f.png)

Solution 5:

kubectl create deployment --image=redis messaging-app

![image](https://user-images.githubusercontent.com/87436052/126132818-8173501b-f3c3-4c93-b396-5a6d9205def1.png)

kubectl expose deployment messaging-app --port=6379 --type=ClusterIP --name=messaging-service

![image](https://user-images.githubusercontent.com/87436052/126132918-e87fd549-8208-4f93-beaa-95f74b94bd3a.png)

Solution 7:  (file Also Upload To Git AS: "hr-web-app-deploy-with-2-replica.yaml" )

Link : https://github.com/ZahiCohen/JB/blob/main/hr-web-app-deploy-with-2-replica.yaml

kubectl create -f "C:\Users\zahi_c\Desktop\hr-web-app-deploy-with-2-replica.yaml"

Yaml File:

![image](https://user-images.githubusercontent.com/87436052/126060656-9a3056d8-f09a-42f0-bc97-bfd9588f390e.png)

![image](https://user-images.githubusercontent.com/87436052/126060481-07243b43-6e2c-4f07-b8e2-903fa702c637.png)

kubectl get replicaset

![image](https://user-images.githubusercontent.com/87436052/126060491-84876acf-61a7-4358-b90c-9c853e621257.png)

Solution 8: 

1. How to find master node:  
 
kubectl get nodes

![image](https://user-images.githubusercontent.com/87436052/126146046-5bdfb40b-4c5c-4a06-8478-8e1526b69200.png)

2. run on master node:

yaml file: https://github.com/ZahiCohen/JB/blob/main/static-busybox.yaml

kubectl run --restart=Never --image=busybox static-busybox -o yaml --command -- sleep 1000 > /etc/kubernetes/manifests/static-busybox.yaml

![image](https://user-images.githubusercontent.com/87436052/126146250-911b55ec-53bf-458c-b549-ce64c2da9973.png)

![image](https://user-images.githubusercontent.com/87436052/126146404-b96ef533-0eef-48ee-afc8-204c31fe795c.png)

Solution 9:

kubectl create namespace finance-zahicohen

![image](https://user-images.githubusercontent.com/87436052/126065284-f059172b-18fa-4ce7-91f1-af07a5936aee.png)

kubectl run temp-bus --image=redis --port=8080 -n finance-zahicohen

![image](https://user-images.githubusercontent.com/87436052/126147707-7feb3026-efc6-4800-9bd7-4be768c67657.png)

Verfiy :

kubectl get pods --namespace finance-zahicohen

![image](https://user-images.githubusercontent.com/87436052/126147538-00e85029-e342-4d3e-a994-cb308bd05834.png)

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126065622-1ea08254-0faa-42e9-8ab8-8c8c230f8696.png)

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




















