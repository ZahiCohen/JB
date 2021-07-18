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
Solution 7:
kubectl create -f rs.yaml
Yaml File:
![image](https://user-images.githubusercontent.com/87436052/126060513-164834e6-41d1-4947-80af-dfb0ceef5c36.png)

![image](https://user-images.githubusercontent.com/87436052/126060481-07243b43-6e2c-4f07-b8e2-903fa702c637.png)

kubectl get replicaset
![image](https://user-images.githubusercontent.com/87436052/126060491-84876acf-61a7-4358-b90c-9c853e621257.png)


