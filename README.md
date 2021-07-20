# JB
------------
מטלה מסכמת גון ברייס
----------------------------

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
-----------------------

1. kubectl get pods --show-labels

![image](https://user-images.githubusercontent.com/87436052/126289175-d8e3afc6-bca3-4cb2-9615-b3d503704b10.png)

2. nginx x 5 with label

kubectl run nginx-1 --image=nginx --labels env=prod
kubectl run nginx-2 --image=nginx --labels env=prod
kubectl run nginx-3 --image=nginx --labels env=dev
kubectl run nginx-4 --image=nginx --labels env=dev
kubectl run nginx-5 --image=nginx --labels env=dev

![image](https://user-images.githubusercontent.com/87436052/126293909-b06b4bed-28e0-46e0-85f4-17058beb42e3.png)


3. kubectl get pods --show-labels 

![image](https://user-images.githubusercontent.com/87436052/126294234-0431b6aa-7610-4cce-9885-95f237a2dfa0.png)

4. kubectl get pods -l env=dev

![image](https://user-images.githubusercontent.com/87436052/126294372-8b3d51c4-7dbd-46e0-bde3-da7370db759a.png)

5. kubectl get pods -l env=dev --show-labels

![image](https://user-images.githubusercontent.com/87436052/126296691-54e64670-50bd-45bc-9ae8-dd1fb1769682.png)

6. kubectl get pods -l env=prod

![image](https://user-images.githubusercontent.com/87436052/126296024-8582c894-c192-4e5a-8dc0-2359b84aeda0.png)

7. kubectl get pods -l env=prod

![image](https://user-images.githubusercontent.com/87436052/126296907-859652ed-6c30-41b5-8ea7-1af763d722d5.png)

8. kubectl get pods -l env

![image](https://user-images.githubusercontent.com/87436052/126297046-5465d23c-00c2-4d87-b523-36e88b3aaf1c.png)

9. kubectl get pods -l env --show-labels (testing)

![image](https://user-images.githubusercontent.com/87436052/126298789-e9abe9ca-7c1f-4774-a68e-097d7b945544.png)

10. kubectl get pods -l env --show-labels > output.txt 

11. kubectl label pods nginx-5 env=uat --overwrite

    kubectl get pods -l env --show-labels 
    
    ![image](https://user-images.githubusercontent.com/87436052/126299422-6b7b3161-f69a-4998-ad3a-d1ca560ca4a4.png)


12. kubectl label pods -l env env

kubectl get pods --show-labels 

![image](https://user-images.githubusercontent.com/87436052/126301721-0fc4e5a8-0638-4c69-9ed6-fd45c154f5fd.png)


![image](https://user-images.githubusercontent.com/87436052/126301886-e8725df2-bee8-4abc-a048-e2669c3f219c.png)

13. kubectl label pods --all app=nginx --overwrite

kubectl get pods --show-labels

![image](https://user-images.githubusercontent.com/87436052/126303143-47cb54a8-13c7-4b19-9a35-cbd2192fa69f.png)


14. kubectl get nodes --show-labels

![image](https://user-images.githubusercontent.com/87436052/126303437-d0d2b3b7-ba97-4299-9c55-9ea39e9b5d7a.png)

15. kubectl label nodes minikube nodeName=nginxnode

![image](https://user-images.githubusercontent.com/87436052/126303733-a1777f19-94da-4651-bde8-86d13f800263.png)

16. kubectl create -f "C:\Yaml-Files\pod-deploy-node-worker.yaml"

![image](https://user-images.githubusercontent.com/87436052/126304510-a2eeaf7c-c194-4e7a-bf74-f077bde29305.png)

17. kubectl describe pods nginx 

![image](https://user-images.githubusercontent.com/87436052/126305441-195535b2-9f8a-481b-af66-f92ab30bbbda.png)

FIX:

kubectl apply -f "C:\Yaml-Files\pod-deploy-node-worker.yaml"

![image](https://user-images.githubusercontent.com/87436052/126306610-7dc80778-f09f-410e-a52a-191bbd38a4cf.png)

18. kubectl get pods nginx --show-labels

![image](https://user-images.githubusercontent.com/87436052/126305882-f502dce9-2c69-46bd-bb81-589fb7029d7d.png)

DEPLOYMENTS :
------------------

1.  kubectl create -f "C:\Yaml-Files\web-app-deployment-5-replic.yaml"

![image](https://user-images.githubusercontent.com/87436052/126307692-713f5c30-6629-485c-9d5e-47d95661c656.png)

kubectl get deployments webapp 

![image](https://user-images.githubusercontent.com/87436052/126307789-b720b790-b745-4d68-819c-186550ec5135.png)


2. kubectl rollout status deployment webapp 

![image](https://user-images.githubusercontent.com/87436052/126307902-09105de1-1590-479f-92c2-0fa7a6b8692f.png)

3.  kubectl get pods

kubectl get rs webapp-5654c984c

![image](https://user-images.githubusercontent.com/87436052/126308425-a4eb1d21-ddfc-47fc-9296-180b480274bc.png)

4.  EXPORT :

yaml replica :  kubectl get rs webapp-5654c984c -o yaml

![image](https://user-images.githubusercontent.com/87436052/126309048-1b2ba741-3e1f-4345-a11a-0aa4fc47ee08.png)

yaml delpyment webapp

![image](https://user-images.githubusercontent.com/87436052/126309165-f2c379aa-fbe6-4017-9834-f3c086c7aef0.png)


5. 

kubectl delete deploy webapp

kubectl get po -l app=webapp -w

![image](https://user-images.githubusercontent.com/87436052/126310501-329159b8-116e-42f8-851d-e6a2e1019577.png)


















































