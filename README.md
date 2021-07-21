# JB
------------
מטלה מסכמת גון ברייס
----------------------------

המטלה נעשתה על מיניקיוב בווינדוס 10
יש להוריד את קבצי הימל לתקייה ולהריץ בהתאם לנתיב הנכון

גירסת לינוקס:

ubuntu On Windows 10

------------------------------------------------

Question  1

Deploy a pod named nginx-pod using the nginx:alpine image.
Name: nginx-pod-yourname
Image: nginx:alpine

Solution 1 : 

kubectl create -f "C:\Yaml-Files\nginx-pod-zahi.yaml"

yaml file : https://github.com/ZahiCohen/JB/blob/main/nginx-pod-zahi.yaml

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126272697-2c52f137-5329-46fa-9fb0-36481060127e.png)


Question  2

Deploy a messaging pod using the redis:alpine image with the labels set to tier=msg.
Pod Name: messaging
Image: redis:alpine
Labels: tier=msg


Solution 2:

kubectl create -f "C:\Yaml-Files\messaging-pod.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/messaging-pod.yaml

kubectl get pods

kubectl get pods -l "tier=msg"

![image](https://user-images.githubusercontent.com/87436052/126273346-d075ee12-310f-4500-89d8-8393a7601d67.png)

kubectl get pods --show-labels

![image](https://user-images.githubusercontent.com/87436052/126328170-5dc7ace8-26de-42d6-92c2-b2ad7dcc7ca8.png)

Question  3

Create a namespace named apx-x998-yourname

Solution 3:

kubectl create namespace apx-x998-zahi

![image](https://user-images.githubusercontent.com/87436052/126072299-ac068b11-5c1d-484b-8df0-f753f3fb3eaf.png)

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126072318-edcb2d30-54f7-469a-9f7d-418764f35531.png)

Question  4

Get the list of nodes in JSON format and store it in a file at /tmp/nodes-yourname

Solution 4:

kubectl get nodes -o jsonpath='/tmp/nodes-zahi'

![image](https://user-images.githubusercontent.com/87436052/126060293-758bcbf2-3d9a-486d-a0cc-bc3d8afd172f.png)

Question 5

Create a service messaging-service to expose the messaging application within the
cluster on port 6379.
a. Use imperative commands - kubectl
b. Service: messaging-service
c. Port: 6379
d. Type: ClusterIp
e. Use the right labels

Solution 5:

kubectl create -f "C:\Yaml-Files\messaging-service.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/messaging-service.yaml

kubectl get svc

![image](https://user-images.githubusercontent.com/87436052/126273857-dcb677ef-5109-42c0-8717-e221c5684ba9.png)

kubectl get svc --show-labels

![image](https://user-images.githubusercontent.com/87436052/126443526-a18cf812-99ea-41d8-8357-e041dc98595b.png)

Question 7

Create a deployment named hr-web-app using the image kodekloud/webapp-color
with 2 replicas
a. Name: hr-web-app
b. Image: kodekloud/webapp-color
c. Replicas: 2

Solution 7: 

kubectl create -f "C:\Yaml-Files\hr-web-app-deploy.yaml"

yaml file https://github.com/ZahiCohen/JB/blob/main/hr-web-app-deploy.yaml

kubectl get pods

kubectl get replicaset

![image](https://user-images.githubusercontent.com/87436052/126274700-41bcfb87-c0f1-4e47-98a5-62c741a64708.png)

Question 8

Create a static pod named static-busybox on the master node that uses the busybox
image and the command sleep 1000
a. Name: static-busybox
b. Image: busybox

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

Question 9

Create a POD in the finance-yourname namespace named temp-bus with the image
redis:alpine
a. Name: temp-bus
b. Image Name: redis:alpine

Solution 9:

kubectl create -f "C:\Yaml-Files\create-finance-pod.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/create-finance-pod.yaml

kubectl get namespace

![image](https://user-images.githubusercontent.com/87436052/126275804-223bae65-7d49-4d3d-9696-84657a36e131.png)

kubectl get pods --namespace finance-zahi

![image](https://user-images.githubusercontent.com/87436052/126275837-60bd69b0-3932-40cc-9320-c9d7fe61007c.png)

Question 10

Create a Persistent Volume with the given specification
a. Volume Name: pv-analytics
b. Storage: 100Mi
c. Access modes: ReadWriteMany
d. Host Path: /pv/data-analytics

Solution 10: 

kubectl create -f "C:\Yaml-Files\persisten-vol.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/persisten-vol.yaml

kubectl get pv

![image](https://user-images.githubusercontent.com/87436052/126276667-8dde514b-e61f-4382-b566-28c8111597c3.png)

Question 11

Create a Pod called redis-storage-yourname with image: redis:alpine with a Volume
of type emptyDir that lasts for the life of the Pod. specs:.
a. Pod named 'redis-storage-yourname'
b. Pod 'redis-storage-yourname' uses Volume type of emptyDir
c. Pod 'redis-storage-yourname' uses volumeMount with mountPath =
/data/redis

Solution 11:

kubectl create -f "C:\Yaml-Files\redis-storage-zahi-pod.yaml"

yaml file : https://github.com/ZahiCohen/JB/blob/main/redis-storage-zahi-pod.yaml

![image](https://user-images.githubusercontent.com/87436052/126277072-e2f0d87a-19ff-49f9-8798-9fd79e5ae3ad.png)

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126277135-f52c63dc-33ee-43e8-b78e-76af78b8473e.png)

Question 12

Create this pod and attached it a persistent volume called pv-1
a. Make sure the PV mountPath is hostbase : /data

Solution 12:

kubectl create -f "C:\Yaml-Files\nginx-pod-attach.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/nginx-pod-attach.yaml

kubectl get pv pv-1

kubectl get pvc pv-1

kubectl get pods use-pv-zahi

![image](https://user-images.githubusercontent.com/87436052/126277986-64ea7098-ab4e-4885-a4e1-3d31771ed067.png)

Question 13

Create a new deployment called nginx-deploy, with image nginx:1.16 and 1 replica.
Record the version. Next upgrade the deployment to version 1.17 using rolling
update. Make sure that the version upgrade is recorded in the resource annotation.
a. Deployment : nginx-deploy. Image: nginx:1.16
b. Image: nginx:1.16
c. Task: Upgrade the version of the deployment to 1:17
d. Task: Record the changes for the image upgrade

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

Question 14

Create an nginx pod called nginx-resolver using image nginx, expose it internally
with a service called nginx-resolver-service. Test that you are able to look up the 
service and pod names from within the cluster. Use the image: busybox:1.28 for dns
lookup. Record results in /root/nginx-yourname.svc and /root/nginx-yourname.pod

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

Question 15

Create a static pod on node01 called nginx-critical with image nginx. Create this pod
on node01 and make sure that it is recreated/restarted automatically in case of a
failure.

Solution 15: (skipped ) Can Not Apply in minikube found info here :

https://kubernetes.io/docs/tasks/configure-pod-container/static-pod/

Question 16

Create a pod called multi-pod with two containers.
Container 1, name: alpha, image: nginx
Container 2: beta, image: busybox, command sleep 4800.
a. Environment Variables:
i. container 1:
ii. name: alpha
iii. Container 2:
iv. name: beta

Solution 16:

kubectl create -f "C:\Yaml-Files\multi-pod.yaml"

yaml file : https://github.com/ZahiCohen/JB/blob/main/multi-pod.yaml

kubectl get pods

kubectl describe pods multi-pod

![image](https://user-images.githubusercontent.com/87436052/126284734-d5f17ca0-8cf2-4f01-a5d0-2426ee811f01.png)


![image](https://user-images.githubusercontent.com/87436052/126284930-55688e2a-c632-4335-bdfb-7fd52c20e2fe.png)


Pod Design Answres:
-----------------------
1. Type the command for: Get pods with label information

Solution 1:

kubectl get pods --show-labels

![image](https://user-images.githubusercontent.com/87436052/126455572-5004d51f-5144-46e9-8005-927593f376a8.png)

2. Create 5 nginx pods in which two of them is labeled env=prod and three of them is
labeled env=dev

Solution 2:

kubectl run nginx-1 --image=nginx --labels env=prod

kubectl run nginx-2 --image=nginx --labels env=prod

kubectl run nginx-3 --image=nginx --labels env=dev

kubectl run nginx-4 --image=nginx --labels env=dev

kubectl run nginx-5 --image=nginx --labels env=dev

![image](https://user-images.githubusercontent.com/87436052/126293909-b06b4bed-28e0-46e0-85f4-17058beb42e3.png)

3. Verify all the pods are created with correct labels

Solution 3:

kubectl get pods --show-labels 

![image](https://user-images.githubusercontent.com/87436052/126455812-37b3e965-76cf-4b5b-9988-56631e899272.png)

4. Get the pods with label env=dev

Solution 4:

kubectl get pods -l env=dev

![image](https://user-images.githubusercontent.com/87436052/126294372-8b3d51c4-7dbd-46e0-bde3-da7370db759a.png)

5. Get the pods with label env=dev and also output the labels

Solution 5:

kubectl get pods -l env=dev --show-labels

![image](https://user-images.githubusercontent.com/87436052/126296691-54e64670-50bd-45bc-9ae8-dd1fb1769682.png)

Solution 6:

Get the pods with label env=prod

6. kubectl get pods -l env=prod

![image](https://user-images.githubusercontent.com/87436052/126296024-8582c894-c192-4e5a-8dc0-2359b84aeda0.png)

7. Get the pods with label env=prod and also output the labels

Solution 7:

kubectl get pods -l env=prod --show-labels

![image](https://user-images.githubusercontent.com/87436052/126296907-859652ed-6c30-41b5-8ea7-1af763d722d5.png)

8. Get the pods with label env

Solution 8:

kubectl get pods -l env

![image](https://user-images.githubusercontent.com/87436052/126297046-5465d23c-00c2-4d87-b523-36e88b3aaf1c.png)

9. Get the pods with labels env=dev and env=prod

Solution 9 : Run On minikube cmd 

kubectl get pods -l env=dev & kubectl get pods -l env=prod

![image](https://user-images.githubusercontent.com/87436052/126457542-aed0c847-1a4c-4446-a9a5-41ecbc1bd616.png)

10. Get the pods with labels env=dev and env=prod and output the labels as well

Solution 10: Run On minikube cmd 

kubectl get pods -l env=dev --show-labels & kubectl get pods -l env=prod --show-labels

![image](https://user-images.githubusercontent.com/87436052/126457091-58908b93-e93b-429a-ab3f-d9ed8aa0feaf.png)

11. Change the label for one of the pod to env=uat and list all the pods to verify

Solution 11:

kubectl label pods nginx-5 env=uat --overwrite

kubectl get pods -l env --show-labels 

![image](https://user-images.githubusercontent.com/87436052/126458307-88f85b3f-2bf3-4c5e-b826-48a801fcd613.png)

12. Remove the labels for the pods that we created now and verify all the labels are
removed

Solution 12:

kubectl label pods -l env env-

kubectl get pods --show-labels 

![image](https://user-images.githubusercontent.com/87436052/126458531-4e4e702e-b76d-4b57-9f92-2302ee722067.png)

![image](https://user-images.githubusercontent.com/87436052/126458574-7468a97b-4c49-465b-976e-4690b5561329.png)

13. Let’s add the label app=nginx for all the pods and verify (using kubectl)

Solution 13:

 kubectl label pods --all app=nginx --overwrite

 ### for deployment the command is " kubectl label deployment --all app=nginx --overwrite "

kubectl get pods --show-labels

![image](https://user-images.githubusercontent.com/87436052/126460481-db646579-9a8a-45b1-8d36-2bc3363861a0.png)

14. Get all the nodes with labels (if using minikube you would get only master node)

Solution 14:

kubectl get nodes --show-labels

![image](https://user-images.githubusercontent.com/87436052/126460784-a8c84bae-d248-4a8b-b7bc-45afcaffd956.png)

15. Label the worker node nodeName=nginxnode

Solution 15:

command : kubectl label nodes (worker node name here) nodeName=nginxnode

Run On MiniKube 1 node:

kubectl label nodes minikube nodeName=nginxnode

![image](https://user-images.githubusercontent.com/87436052/126460991-42d2243c-68aa-4c37-9427-b1ad271ddf41.png)

16. Create a Pod that will be deployed on the worker node with the label
nodeName=nginxnode
Add the nodeSelector to the below and create the pod

Solution 16:

kubectl create -f "C:\Yaml-Files\pod-deploy-node-worker.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/pod-deploy-node-worker.yaml

![image](https://user-images.githubusercontent.com/87436052/126461984-fb501114-a5e2-467e-9cfb-e3d4f5b0e2ee.png)

kubectl get pods -l nodeName

kubectl get pods -l nodeName --show-labels

![image](https://user-images.githubusercontent.com/87436052/126462321-98440304-a8ff-4e57-b1ce-f0d26d404650.png)

17. Verify the pod that it is scheduled with the node selector on the right node… fix it if
it’s not behind scheduled. 

Solution 17:

kubectl describe pods nginx 

![image](https://user-images.githubusercontent.com/87436052/126305441-195535b2-9f8a-481b-af66-f92ab30bbbda.png)

FIX:

kubectl apply -f "C:\Yaml-Files\pod-deploy-node-worker.yaml" 

yaml file: https://github.com/ZahiCohen/JB/blob/main/pod-deploy-node-worker.yaml

![image](https://user-images.githubusercontent.com/87436052/126306610-7dc80778-f09f-410e-a52a-191bbd38a4cf.png)

18. Verify the pod nginx that we just created has this label

Solution 18:

kubectl get pods -l nodeName=nginxnode --show-labels

![image](https://user-images.githubusercontent.com/87436052/126463388-781b551b-1755-49ef-9ea1-a698f13e05f2.png)

DEPLOYMENTS :
------------------
1. Create a deployment called webapp with image nginx with 5 replicas
a. Use the below command to create a yaml file.
i. kubectl create deploy webapp --image=nginx --dry-run -o yaml >
webapp.yaml
ii. Edit it and add 5 replica’s

1.  

kubectl create -f "C:\Yaml-Files\web-app-deployment-5-replic.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/web-app-deployment-5-replic.yaml

![image](https://user-images.githubusercontent.com/87436052/126307692-713f5c30-6629-485c-9d5e-47d95661c656.png)

kubectl get deployments webapp 

![image](https://user-images.githubusercontent.com/87436052/126307789-b720b790-b745-4d68-819c-186550ec5135.png)

2. Get the deployment rollout status

2. 

kubectl rollout status deployment webapp 

![image](https://user-images.githubusercontent.com/87436052/126307902-09105de1-1590-479f-92c2-0fa7a6b8692f.png)

3. Get the replicaset that created with this deployment

3.  

kubectl get rs -l app=webapp

![image](https://user-images.githubusercontent.com/87436052/126464446-f2ebb89d-84e8-478d-8547-ae56e861857a.png)

4. EXPORT the yaml of the replicaset and pods of this deployment

4.  

kubectl get rs -l app=webapp -o yaml

kubectl get pods -l app=webapp -o yaml

![image](https://user-images.githubusercontent.com/87436052/126465591-97616368-935d-4b4d-ab92-4c09620bdf4a.png)

![image](https://user-images.githubusercontent.com/87436052/126465788-1a3f5598-b134-4b1b-ba16-39af25b8c74f.png)

5. Delete the deployment you just created and watch all the pods are also being
deleted

5. 

kubectl delete deploy webapp

kubectl get pod -l app=webapp -w

![image](https://user-images.githubusercontent.com/87436052/126310501-329159b8-116e-42f8-851d-e6a2e1019577.png)

6. Create a deployment of webapp with image nginx:1.17.1 with container port 80 and
verify the image version
a. kubectl create deploy webapp --image=nginx:1.17.1 --dry-run -o yaml >
webapp.yaml
b. add the port section (80) and create the deployment

6.  

kubectl create deploy webapp --image=nginx:1.17.1 --dry-run -o yaml

![image](https://user-images.githubusercontent.com/87436052/126314281-cce93f36-b6ee-4e44-98fb-37e536f5bc19.png)

![image](https://user-images.githubusercontent.com/87436052/126314448-cb3a081c-1d88-4b96-a072-50a84f53f206.png)

kubectl create -f "C:\Yaml-Files\web-app-deploy-nginx-1.17.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/web-app-deploy-nginx-1.17.yaml

![image](https://user-images.githubusercontent.com/87436052/126314569-775b33c8-c2f3-4fbd-830b-dbd5a0ae4604.png)

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126314716-d5651f35-13f9-428b-9741-cc7cb7c4ed90.png)

7. Update the deployment with the image version 1.17.4 and verify

7.

kubectl set image deploy/webapp nginx=nginx:1.17.4

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126314877-27c8c71c-21ae-4492-9a35-8bcdc0c3096e.png)

![image](https://user-images.githubusercontent.com/87436052/126314908-9ab4f1b9-dfe5-4ddf-893b-d74495751600.png)

8. Check the rollout history and make sure everything is ok after the update

8.   

kubectl rollout history deploy webapp

kubectl get deploy webapp --show-labels

kubectl get rs -l app=webapp

kubectl get po -l app=webapp

![image](https://user-images.githubusercontent.com/87436052/126315068-a56cdbe1-9aac-4b00-9692-cfd5c3c9385b.png)

9. Undo the deployment to the previous version 1.17.1 and verify Image has the
previous version

9.

kubectl rollout undo deploy webapp

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126315505-81042a6a-25a7-4fa2-ad4a-566080fa5db6.png)

10. Update the deployment with the wrong image version 1.100 and verify something is
wrong with the deployment
a. Expect: kubectl get pods (ImagePullErr)
b. Undo the deployment with the previous version and verify everything is Ok
c. kubectl rollout history deploy webapp --revision=7
d. Check the history of the specific revision of that deployment
e. update the deployment with the image version latest and check the history
and verify nothing is going on

10.

a.

kubectl set image deploy/webapp nginx=nginx:1.100

kubectl rollout status deploy webapp

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126316307-b1e68317-ec34-48a0-96df-e88380eac34c.png)

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126469540-5b6e16fa-9abe-4343-8b8e-b6b60b8a7e03.png)


b.

kubectl rollout undo deploy webapp

kubectl rollout status deploy webapp

kubectl get pods

![image](https://user-images.githubusercontent.com/87436052/126316607-69be820c-0234-46c5-a3f3-071562679122.png)

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126470595-4c95a7ec-ac6b-40cc-bc8b-78692956846e.png)

c.

kubectl rollout history deploy webapp --revision=7

![image](https://user-images.githubusercontent.com/87436052/126471104-7f67f278-0e68-445d-aee5-46ef52a92781.png)

d.

kubectl rollout history deploy webapp

kubectl rollout history deployment webapp --revision=2

kubectl rollout history deployment webapp --revision=4

kubectl rollout history deployment webapp --revision=5

![image](https://user-images.githubusercontent.com/87436052/126473367-d18b6684-838c-4ae1-8908-ccdc9cf97108.png)

e.

kubectl set image deploy/webapp nginx=nginx:latest

kubectl rollout history deploy webapp

kubectl describe deploy webapp

![image](https://user-images.githubusercontent.com/87436052/126317265-cd8d5d4c-8a69-40a3-9693-26b7f9838f33.png)

kubectl rollout history deployment webapp --revision=6

![image](https://user-images.githubusercontent.com/87436052/126474072-6a2f6bbf-5e41-4a22-b756-e9582be99ba4.png)

kubectl get deploy webapp

kubectl describe webapp

![image](https://user-images.githubusercontent.com/87436052/126474236-cb8aebb4-07c6-4d6f-9a70-3ad47de9eb84.png)

11. Apply the autoscaling to this deployment with minimum 10 and maximum 20 replicas
and target CPU of 85% and verify hpa is created and replicas are increased to 10
from 1

11.

kubectl autoscale deploy webapp --min=10 --max=20 --cpu-percent=85

kubectl get hpa

kubectl get pod -l app=webapp

![image](https://user-images.githubusercontent.com/87436052/126318540-45e15b42-16bd-488c-935d-c8189c96cd63.png)

13. Clean the cluster by deleting deployment and hpa you just created

13.

kubectl delete deploy webapp

kubectl delete hpa webapp

![image](https://user-images.githubusercontent.com/87436052/126318658-95628a89-e30b-4289-8945-0cf5a9fe0158.png)

14. Create a job and make it run 10 times one after one (run > exit > run >exit ..) using
the following configuration:
kubectl create job hello-job --image=busybox --dry-run -o yaml -- echo "Hello I am
from job" > hello-job.yaml”
a. Add to the above job completions: 10 inside the yaml

14.

kubectl create job hello-job --image=busybox --dry-run -o yaml -- echo "Hello I am from job"

![image](https://user-images.githubusercontent.com/87436052/126318955-d7e334f3-5634-4616-9cc3-cead1d7b7bf7.png)


kubectl create -f "C:\Yaml-Files\hello-job.yaml"

yaml file: https://github.com/ZahiCohen/JB/blob/main/hello-job.yaml

![image](https://user-images.githubusercontent.com/87436052/126319269-b726db70-74d1-47e7-984b-bf2fd723a8a9.png)


CONFIG MAP  
================
1. Create a file called config.txt with two values key1=value1 and key2=value2 and
verify the file

1.  

cat >> config.txt << EOF
key1=value1
key2=value2
EOF

cat config.txt

![image](https://user-images.githubusercontent.com/87436052/126320316-16601806-c448-478e-ae8f-9a52d1e4966d.png)

2. Create a configmap named keyvalcfgmap and read data from the file config.txt and
verify that configmap is created correctly


2.

kubectl create cm keyvalcfgmap --from-file=config.txt

kubectl get cm keyvalcfgmap -o yaml

3. Create an nginx pod and load environment values from the above configmap
keyvalcfgmap and exec into the pod and verify the environment variables and delete
the pod
// first run this command to save the pod yml
kubectl run nginx --image=nginx --restart=Never --dry-run -o yaml > nginx-pod.yml

3. 

kubectl run nginx --image=nginx --restart=Never --dry-run -o yaml

![image](https://user-images.githubusercontent.com/87436052/126321016-654fbf5a-c792-4bbd-a1f1-a0aeb09af9ec.png)

 kubectl create -f "C:\Yaml-Files\config-map-nginx.yaml"
 
 yaml file : https://github.com/ZahiCohen/JB/blob/main/config-map-nginx.yaml

![image](https://user-images.githubusercontent.com/87436052/126320879-ae761b76-1070-49bd-b758-da89ee69a891.png)

verify and delete :
--------------------

kubectl exec -it nginx -- env

kubectl delete pod nginx

![image](https://user-images.githubusercontent.com/87436052/126321711-4bebdbe9-0e36-4188-9f4e-8e60a7fdcde7.png)


Done :)))))))))))
---------------------






































































