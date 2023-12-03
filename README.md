#### Complete Deep Learning Project implementation using MLflow and DVC with CICD deplyment on AWS

# workflow


1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml

## MLflow

- [Documentation](https://mlflow.org/docs/latest/index.html)

##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)


Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=< your MLFLOW_TRACKING_URI >

export MLFLOW_TRACKING_USERNAME=< your MLFLOW_TRACKING_USERNAME > 

export MLFLOW_TRACKING_PASSWORD=< your MLFLOW_TRACKING_PASSWORD>

###  DVC  commands 

dvc init
dvc repro
dvc dag

### image encode and decode reference:

https://base64.guru/converter/encode/image
https://base64.guru/converter/decode/image

# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: your URI from AWS 

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one

	inside github runners find following commands, run them one by one aws EC3 cli:

	Download--   run all those commands



Configure--  run all those commands
# Create the runner and start the configuration experience
$ ./config.sh --url https://github.com/Sushanth172308/DeepLearning-Project-MLflow-DVC-CICD --token <your token> # Last step, run it!
$ ./run.sh

Enter the name of runner:self-hosted



# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION =

    AWS_ECR_LOGIN_URI =

    ECR_REPOSITORY_NAME = 
