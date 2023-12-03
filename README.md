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