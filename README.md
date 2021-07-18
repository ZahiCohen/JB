# JB
מטלה מסכמת גון ברייס

Solution 1 : kubectl run nginx-pod-zahi --image alpine/nginx:latest –-port=8080

![image](https://user-images.githubusercontent.com/87436052/126059999-53b6ea01-dd55-42b9-baf3-c85cecddde5d.png)

![image](https://user-images.githubusercontent.com/87436052/126060011-4dd7a9aa-d727-4815-a8e5-49d84787603d.png)


Solution 2:

kubectl run messaging --image alpine/redis --labels="tier=msg"

![image](https://user-images.githubusercontent.com/87436052/126060222-f81b2f0a-4349-467d-9a07-d81657d740c2.png)

Solution 3:

kubectl create namespace apx-x998-zahi

![image](https://user-images.githubusercontent.com/87436052/126060280-ee334694-bc19-4539-8f2f-fdece0c56b3e.png)

Solution 4:

kubectl get nodes -o jsonpath='/tmp/nodes-zahi'

![image](https://user-images.githubusercontent.com/87436052/126060293-758bcbf2-3d9a-486d-a0cc-bc3d8afd172f.png)

Solution 5:

kubectl expose deployment messaging –-port=6379 --type=ClusterIp --name=messaging-service

Solution 7:  (file Also Upload To Git AS: "hr-web-app-deploy-with-2-replica.yaml"

kubectl create -f hr-web-app-deploy-with-2-replica.yaml

Yaml File:

![image](https://user-images.githubusercontent.com/87436052/126060656-9a3056d8-f09a-42f0-bc97-bfd9588f390e.png)

![image](https://user-images.githubusercontent.com/87436052/126060481-07243b43-6e2c-4f07-b8e2-903fa702c637.png)

kubectl get replicaset

![image](https://user-images.githubusercontent.com/87436052/126060491-84876acf-61a7-4358-b90c-9c853e621257.png)

Solution 8: לבדיקה

How to find master node from worker node in Kubernetes

![image](https://user-images.githubusercontent.com/87436052/126064906-f6b93398-004f-4008-82f8-dddfefb3b234.png)


OR :

![image](https://user-images.githubusercontent.com/87436052/126064911-8c5a7645-51cd-4e76-aa21-3265fb2b838e.png)


https://kubernetes.io/docs/tasks/configure-pod-container/static-pod/

Solution 9:

kubectl create namespace finance-zahicohen

kubectl run temp-bus --image alpine/redis --port=8080 -n finance-zahicohen

![image](https://user-images.githubusercontent.com/87436052/126065284-f059172b-18fa-4ce7-91f1-af07a5936aee.png)

![image](https://user-images.githubusercontent.com/87436052/126065291-8cfad346-9fc1-47aa-b6ef-2863bb58ac7b.png)

Verfiy :

kubectl get pods

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126065622-1ea08254-0faa-42e9-8ab8-8c8c230f8696.png)







