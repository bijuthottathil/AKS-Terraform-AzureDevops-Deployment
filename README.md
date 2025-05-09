# AKSwithADO

1) CD Infra
2) Terraform init ![image](https://github.com/user-attachments/assets/ba7744dd-992f-4af5-adaa-145727a19ffb)
3) Logged in to Azure using Az login


![image](https://github.com/user-attachments/assets/1b464364-d52e-4b30-8bcb-1b820077d44b)
Used Terraform to deploy infrastructure

4) Compile Flask service 
5 ) Next Build & Push Docker Image to the Azure Container Registry

docker push bijuregristrynew.azurecr.io/flask-api:latest  
(3.10.12) bijum@MacBook-Pro infra % docker push bijuthottathil/flask-api:latest   Azure Registry created 
![image](https://github.com/user-attachments/assets/3bdb6bd9-21cd-4d2c-8a1d-602ad4fc2e53)   



Deploy Flask App Using Helm

![image](https://github.com/user-attachments/assets/1a266c31-f18e-4aec-83bd-a1dab0cac61d)

1 cd ..
2 cd helm
3 cd flask-chart
4  ls
Chart.yaml      templates       values.yaml
5  helm upgrade --install flask-app . \
  --set image.repository=bijuthottathil/flask-api \
  --set image.tag=latest
Release "flask-app" does not exist. Installing it now.
NAME: flask-app
LAST DEPLOYED: Fri May  9 11:03:05 2025
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
    


Set Up Azure DevOps CI/CD Pipeline

![image](https://github.com/user-attachments/assets/7a014646-45ac-4f7a-a9c5-ffae865755f0)



create pipe line

![image](https://github.com/user-attachments/assets/b5536eaa-1286-4a51-a8c8-1f01042f72e1)

Appropriate service connections are set in Azure Devops to connect to ACR and Azure
![image](https://github.com/user-attachments/assets/bb153257-5851-4bdc-8a4c-28b8c01f6a9f)

Once I initiate to run pipeline, this is the log generated

![image](https://github.com/user-attachments/assets/eff6f78f-fd81-4b29-9c74-e909e65c7a65)


![image](https://github.com/user-attachments/assets/3a0aa55f-5f47-48ca-b44e-1d6f5b28158f)
![image](https://github.com/user-attachments/assets/a0c22d63-89b4-449e-8286-e1776d76ae6e)

In below screenshot, you can see service is running in AKS, Using loadbalance IP , you can the response came from the service installed in Kubernetes Cluster

(3.10.12) bijum@MacBook-Pro infra % curl  http://48.216.198.239/                    
Hello, World from Flask on AKS!%  

![image](https://github.com/user-attachments/assets/7689c764-23e0-47c7-b4c4-31495ecd44cf)

Even I port forwarded service to 8080 port,

(3.10.12) bijum@MacBook-Pro infra % kubectl port-forward svc/flask-service 8080:80          

Forwarding from [::1]:8080 -> 5000
Handling connection for 8080
Handling connection for 8080

Based on this, I am able to access microservice in browser too
![image](https://github.com/user-attachments/assets/f7cd29af-69cd-4832-996a-cbbb04149df2)

