# AKSwithADO

1) CD Infra
2) Terraform init ![image](https://github.com/user-attachments/assets/ba7744dd-992f-4af5-adaa-145727a19ffb)
3) Logged in to Azure using Az login
4) 

![image](https://github.com/user-attachments/assets/1b464364-d52e-4b30-8bcb-1b820077d44b)


Next Build & Push Docker Image
Time being I buil docker image  and push to my git docker hub ![image](https://github.com/user-attachments/assets/a3f96872-a3b0-4015-b73b-110c49f2c521)

![image](https://github.com/user-attachments/assets/eac299c5-7068-4e14-b326-1d48abd821ac)

Deploy Flask App Using Helm

![image](https://github.com/user-attachments/assets/1a266c31-f18e-4aec-83bd-a1dab0cac61d)

(3.10.12) bijum@MacBook-Pro app % cd ..
(3.10.12) bijum@MacBook-Pro AKSwithADO % cd helm
(3.10.12) bijum@MacBook-Pro helm % cd flask-chart
(3.10.12) bijum@MacBook-Pro flask-chart % ls
Chart.yaml      templates       values.yaml
(3.10.12) bijum@MacBook-Pro flask-chart % helm upgrade --install flask-app . \
  --set image.repository=bijuthottathil/flask-api \
  --set image.tag=latest
Release "flask-app" does not exist. Installing it now.
NAME: flask-app
LAST DEPLOYED: Fri May  9 11:03:05 2025
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
(3.10.12) bijum@MacBook-Pro flask-chart %     


Set Up Azure DevOps CI/CD Pipeline

![image](https://github.com/user-attachments/assets/7a014646-45ac-4f7a-a9c5-ffae865755f0)

create pipe line

![image](https://github.com/user-attachments/assets/b5536eaa-1286-4a51-a8c8-1f01042f72e1)

![image](https://github.com/user-attachments/assets/3a0aa55f-5f47-48ca-b44e-1d6f5b28158f)


![image](https://github.com/user-attachments/assets/7689c764-23e0-47c7-b4c4-31495ecd44cf)
