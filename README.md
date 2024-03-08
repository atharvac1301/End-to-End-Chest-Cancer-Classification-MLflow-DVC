# End-to-End-Chest-Cancer-Classification-MLflow-DVC


## Workflows

1. Update config.yaml
2. Update secrets.yaml [optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml


## MLflow
- [Docs](https://www.mlflow.org/docs/2.3.1/index.html#)

#### cmd
- mlflow ui


### Dagshub
[dagshub](https://dagshub.com/)


```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/atharvac1301/End-to-End-Chest-Cancer-Classification-MLflow-DVC.mlflow

export MLFLOW_TRACKING_USERNAME=atharvac1301

export MLFLOW_TRACKING_PASSWORD=fcc56715d30099c587b900a8711bff8195c6cc1a


```

## DVC cmd
1. dvc init
2. dvc repro
3. dvc dag


# AWS-CI/CD-Deployment-with-Github-Actions
## 1. Login to AWS Console
## 2. Create IAM user for deployment


```bash
# with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container Registry to save your docker image in AWS


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Launch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess

```

## 3. Create ECR repo to store/save docker image
```bash
- Save the URI: 477259042022.dkr.ecr.eu-north-1.amazonaws.com/chest-cancer
```

## 4. Create EC2 Machine (Ubuntu)
## 5. Open EC2 and Install Docker in EC2 Machine:
```bash
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker

```

## 6. Configure EC2 as self-hosted runner:
```bash
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```

## 7. Setup github secrets:
```bash
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = eu-north-1

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = simple-app

```





