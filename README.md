# JB
------------
מטלה מסכמת גון ברייס
----------------------------

המטלה נעשתה על מיניקיוב בווינדוס 10
יש להוריד את קבצי הימל לתקייה ולהריץ בהתאם לנתיב הנכון

גירסת לינוקס:

ubuntu On Windows 10

------------------------------------------------
Solution 1 : 

kubectl create -f "C:\Yaml-Files\nginx-pod-zahi.yaml"

yaml file : https://github.com/ZahiCohen/JB/blob/main/nginx-pod-zahi.yaml

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126272697-2c52f137-5329-46fa-9fb0-36481060127e.png)

Solution 2:

kubectl create -f "C:\Yaml-Files\messaging-pod.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/messaging-pod.yaml

kubectl get pods

kubectl get pods -l "tier=msg"

![image](https://user-images.githubusercontent.com/87436052/126273346-d075ee12-310f-4500-89d8-8393a7601d67.png)

kubectl get pods --show-labels

![image](https://user-images.githubusercontent.com/87436052/126328170-5dc7ace8-26de-42d6-92c2-b2ad7dcc7ca8.png)


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

yaml file: https://github.com/ZahiCohen/JB/blob/main/messaging-service.yaml

kubectl get svc

![image](https://user-images.githubusercontent.com/87436052/126273857-dcb677ef-5109-42c0-8717-e221c5684ba9.png)

kubectl get svc --show-labels

![image](https://user-images.githubusercontent.com/87436052/126443526-a18cf812-99ea-41d8-8357-e041dc98595b.png)

Solution 7: 

kubectl create -f "C:\Yaml-Files\hr-web-app-deploy.yaml"

yaml file https://github.com/ZahiCohen/JB/blob/main/hr-web-app-deploy.yaml

kubectl get pods

kubectl get replicaset

![image](https://user-images.githubusercontent.com/87436052/126274700-41bcfb87-c0f1-4e47-98a5-62c741a64708.png)

Solution 8: 

1. How to find master node:  
 
kubectl get nodes

![image](https://user-images.githubusercontent.com/87436052/126146046-5bdfb40b-4c5c-4a06-8478-8e1526b69200.png)

2. run on master node:

kubectl run --restart=Never --image=busybox static-busybox -o yaml --command -- sleep 1000 > /etc/kubernetes/manifests/static-busybox.yaml

run on minikube with yaml export output :

kubectl run --restart=Never --image=busybox static-busybox -o yaml --command -- sleep 1000

![image](https://user-images.githubusercontent.com/87436052/126146250-911b55ec-53bf-458c-b549-ce64c2da9973.png)

![image](https://user-images.githubusercontent.com/87436052/126445207-2e896b84-80ed-4ba4-8e3e-f9c3673d7ae1.png)

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126445442-dc767d91-f992-4ddb-b0e4-5048f93c42a8.png)

Solution 9:

kubectl create -f "C:\Yaml-Files\create-finance-pod.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/create-finance-pod.yaml

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126275804-223bae65-7d49-4d3d-9696-84657a36e131.png)

kubectl get pods --namespace finance-zahi

![image](https://user-images.githubusercontent.com/87436052/126275837-60bd69b0-3932-40cc-9320-c9d7fe61007c.png)

Solution 10: 

kubectl create -f "C:\Yaml-Files\persisten-vol.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/persisten-vol.yaml

kubectl get pv

![image](https://user-images.githubusercontent.com/87436052/126276667-8dde514b-e61f-4382-b566-28c8111597c3.png)

Solution 11:

kubectl create -f "C:\Yaml-Files\redis-storage-zahi-pod.yaml"

yaml file : https://github.com/ZahiCohen/JB/blob/main/redis-storage-zahi-pod.yaml

![image](https://user-images.githubusercontent.com/87436052/126277072-e2f0d87a-19ff-49f9-8798-9fd79e5ae3ad.png)

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126277135-f52c63dc-33ee-43e8-b78e-76af78b8473e.png)

Solution 12:

kubectl create -f "C:\Yaml-Files\nginx-pod-attach.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/nginx-pod-attach.yaml

kubectl get pv pv-1

kubectl get pvc pv-1

kubectl get pods use-pv-zahi

![image](https://user-images.githubusercontent.com/87436052/126277986-64ea7098-ab4e-4885-a4e1-3d31771ed067.png)

Solution 13:

kubectl create -f "C:\Yaml-Files\nginx-deploy.yaml"

yaml file : https://github.com/ZahiCohen/JB/blob/main/nginx-deploy.yaml  ( spec.replicas defaults to 1 if not specify )

kubectl get deploy

kubectl get pods

kubectl describe deployments nginx-deploy

kubectl set image deployments nginx-deploy nginx=nginx:1.17 --record

![image](https://user-images.githubusercontent.com/87436052/126450692-57b14d2c-87a0-43b4-b01a-e50a5fff1a7d.png)

kubectl describe deployments nginx-deploy

![image](https://user-images.githubusercontent.com/87436052/126449925-48f754cc-aa98-440b-8d70-85b0f8f7dd97.png)

Solution 14:

kubectl create -f "C:\Yaml-Files\nginx-resolver.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/nginx-resolver.yaml

kubectl get svc nginx-resolver-service

kubectl get pods nginx-resolver

kubectl run test-nslookup --image=busybox:1.28 -- nslookup nginx-resolver-service

kubectl logs test-nslookup

![image](https://user-images.githubusercontent.com/87436052/126453392-db3fc400-c174-4215-866c-6d4dd37a4dfe.png)

output result:

kubectl get svc nginx-resolver-service > /root/nginx-zahi.svc

kubectl get pods nginx-resolver > /root/nginx-zahi.pod

run on minikube:

kubectl get svc nginx-resolver-service > nginx-zahi.svc

kubectl get pods nginx-resolver > nginx-zahi.pod

![image](https://user-images.githubusercontent.com/87436052/126453057-74ea6387-7db4-4b8e-b9bf-b7ee4e6c5d0c.png)

Solution 15: (skipped ) Can Not Apply in minikube found info here :

https://kubernetes.io/docs/tasks/configure-pod-container/static-pod/

Solution 16:

kubectl create -f "C:\Yaml-Files\multi-pod.yaml"

yaml file : https://github.com/ZahiCohen/JB/blob/main/multi-pod.yaml

kubectl get pods

kubectl describe pods multi-pod

![image](https://user-images.githubusercontent.com/87436052/126284734-d5f17ca0-8cf2-4f01-a5d0-2426ee811f01.png)


![image](https://user-images.githubusercontent.com/87436052/126284930-55688e2a-c632-4335-bdfb-7fd52c20e2fe.png)


Pod Design Answres:
-----------------------

1. kubectl get pods --show-labels

![image](https://user-images.githubusercontent.com/87436052/126455572-5004d51f-5144-46e9-8005-927593f376a8.png)

2. nginx x 5 with label

kubectl run nginx-1 --image=nginx --labels env=prod

kubectl run nginx-2 --image=nginx --labels env=prod

kubectl run nginx-3 --image=nginx --labels env=dev

kubectl run nginx-4 --image=nginx --labels env=dev

kubectl run nginx-5 --image=nginx --labels env=dev

![image](https://user-images.githubusercontent.com/87436052/126293909-b06b4bed-28e0-46e0-85f4-17058beb42e3.png)


3. kubectl get pods --show-labels 

![image](https://user-images.githubusercontent.com/87436052/126455812-37b3e965-76cf-4b5b-9988-56631e899272.png)

4. kubectl get pods -l env=dev

![image](https://user-images.githubusercontent.com/87436052/126294372-8b3d51c4-7dbd-46e0-bde3-da7370db759a.png)

5. kubectl get pods -l env=dev --show-labels

![image](https://user-images.githubusercontent.com/87436052/126296691-54e64670-50bd-45bc-9ae8-dd1fb1769682.png)

6. kubectl get pods -l env=prod

![image](https://user-images.githubusercontent.com/87436052/126296024-8582c894-c192-4e5a-8dc0-2359b84aeda0.png)

7. kubectl get pods -l env=prod --show-labels

![image](https://user-images.githubusercontent.com/87436052/126296907-859652ed-6c30-41b5-8ea7-1af763d722d5.png)

8. kubectl get pods -l env

![image](https://user-images.githubusercontent.com/87436052/126297046-5465d23c-00c2-4d87-b523-36e88b3aaf1c.png)

9. Run On minikube cmd 

kubectl get pods -l env=dev & kubectl get pods -l env=prod

![image](https://user-images.githubusercontent.com/87436052/126457542-aed0c847-1a4c-4446-a9a5-41ecbc1bd616.png)

10.   Run On minikube cmd 

kubectl get pods -l env=dev --show-labels & kubectl get pods -l env=prod --show-labels

![image](https://user-images.githubusercontent.com/87436052/126457091-58908b93-e93b-429a-ab3f-d9ed8aa0feaf.png)

11. kubectl label pods nginx-5 env=uat --overwrite

    kubectl get pods -l env --show-labels 

![image](https://user-images.githubusercontent.com/87436052/126458307-88f85b3f-2bf3-4c5e-b826-48a801fcd613.png)

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

kubectl get pod -l app=webapp -w

![image](https://user-images.githubusercontent.com/87436052/126310501-329159b8-116e-42f8-851d-e6a2e1019577.png)

6.  kubectl create deploy webapp --image=nginx:1.17.1 --dry-run -o yaml

![image](https://user-images.githubusercontent.com/87436052/126314281-cce93f36-b6ee-4e44-98fb-37e536f5bc19.png)

![image](https://user-images.githubusercontent.com/87436052/126314448-cb3a081c-1d88-4b96-a072-50a84f53f206.png)

kubectl create -f "C:\Yaml-Files\web-app-deploy-nginx-1.17.yaml"

![image](https://user-images.githubusercontent.com/87436052/126314569-775b33c8-c2f3-4fbd-830b-dbd5a0ae4604.png)

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126314716-d5651f35-13f9-428b-9741-cc7cb7c4ed90.png)

7.

kubectl set image deploy/webapp nginx=nginx:1.17.4

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126314877-27c8c71c-21ae-4492-9a35-8bcdc0c3096e.png)

![image](https://user-images.githubusercontent.com/87436052/126314908-9ab4f1b9-dfe5-4ddf-893b-d74495751600.png)

8.   

kubectl rollout history deploy webapp
kubectl get deploy webapp --show-labels
kubectl get rs -l app=webapp
kubectl get po -l app=webapp

![image](https://user-images.githubusercontent.com/87436052/126315068-a56cdbe1-9aac-4b00-9692-cfd5c3c9385b.png)

9.

kubectl rollout undo deploy webapp
kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126315505-81042a6a-25a7-4fa2-ad4a-566080fa5db6.png)

10.

a.

kubectl set image deploy/webapp nginx=nginx:1.100

kubectl rollout status deploy webapp

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126316307-b1e68317-ec34-48a0-96df-e88380eac34c.png)

b.

kubectl rollout undo deploy webapp
kubectl rollout status deploy webapp
kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126316607-69be820c-0234-46c5-a3f3-071562679122.png)

c.

kubectl rollout history deploy webapp --revision=7

kubectl rollout history deploy webapp --revision=2

![image](https://user-images.githubusercontent.com/87436052/126316918-4e779af9-459a-47b3-a92e-093c857d66d9.png)


d.

kubectl rollout history deploy webapp --revision=2

![image](https://user-images.githubusercontent.com/87436052/126317009-ef9ff62b-7082-40c7-9b95-347aab35c7f6.png)


e.

kubectl set image deploy/webapp nginx=nginx:latest

kubectl rollout history deploy webapp

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126317265-cd8d5d4c-8a69-40a3-9693-26b7f9838f33.png)

11.

kubectl autoscale deploy webapp --min=10 --max=20 --cpu-percent=85

kubectl get hpa

kubectl get pod -l app=webapp

![image](https://user-images.githubusercontent.com/87436052/126318540-45e15b42-16bd-488c-935d-c8189c96cd63.png)


13.

kubectl delete deploy webapp

kubectl delete hpa webapp

![image](https://user-images.githubusercontent.com/87436052/126318658-95628a89-e30b-4289-8945-0cf5a9fe0158.png)


14.

kubectl create job hello-job --image=busybox --dry-run -o yaml -- echo "Hello I am from job"

![image](https://user-images.githubusercontent.com/87436052/126318955-d7e334f3-5634-4616-9cc3-cead1d7b7bf7.png)


kubectl create -f "C:\Yaml-Files\hello-job.yaml"

![image](https://user-images.githubusercontent.com/87436052/126319269-b726db70-74d1-47e7-984b-bf2fd723a8a9.png)


CONFIG MAP
================

1.  

cat >> config.txt << EOF
key1=value1
key2=value2
EOF

cat config.txt

![image](https://user-images.githubusercontent.com/87436052/126320316-16601806-c448-478e-ae8f-9a52d1e4966d.png)


2.

kubectl create cm keyvalcfgmap --from-file=config.txt

kubectl get cm keyvalcfgmap -o yaml

3. 

kubectl run nginx --image=nginx --restart=Never --dry-run -o yaml

![image](https://user-images.githubusercontent.com/87436052/126321016-654fbf5a-c792-4bbd-a1f1-a0aeb09af9ec.png)

 kubectl create -f "C:\Yaml-Files\config-map-nginx.yaml"

![image](https://user-images.githubusercontent.com/87436052/126320879-ae761b76-1070-49bd-b758-da89ee69a891.png)

verify and delete

kubectl exec -it nginx -- env

kubectl delete po nginx

![image](https://user-images.githubusercontent.com/87436052/126321711-4bebdbe9-0e36-4188-9f4e-8e60a7fdcde7.png)






































































