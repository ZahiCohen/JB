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

How to find master node

kubectl get nodes

run on master node:
$ kubectl run --restart=Never --image=busybox static-busybox --dry-run=client -o yaml --command -- sleep 1000 > /etc/kubernetes/manifests/static-busybox.yaml

Solution 9:

kubectl create namespace finance-zahicohen

kubectl run temp-bus --image alpine/redis --port=8080 -n finance-zahicohen

![image](https://user-images.githubusercontent.com/87436052/126065284-f059172b-18fa-4ce7-91f1-af07a5936aee.png)

![image](https://user-images.githubusercontent.com/87436052/126065291-8cfad346-9fc1-47aa-b6ef-2863bb58ac7b.png)

Verfiy :

kubectl get pods --namespace finance-zahicohen

![image](https://user-images.githubusercontent.com/87436052/126065699-a4595a1f-d3f5-4ca2-b0a5-53dda6be27c0.png)


kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126065622-1ea08254-0faa-42e9-8ab8-8c8c230f8696.png)

Solution 10: (file Also Upload To Git AS: "Persistent Volume.yaml" )

kubectl create -f "C:\Users\zahi_c\Desktop\Persistent Volume.yaml"

![image](https://user-images.githubusercontent.com/87436052/126069121-3b483d1c-d62a-4293-83ce-37847332c499.png)













