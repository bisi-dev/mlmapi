[![CircleCI](https://dl.circleci.com/status-badge/img/gh/bisi-dev/mlmapi/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/bisi-dev/mlmapi/tree/main)

## MACHINE LEARNING MICROSERVICE API

This Machine learning project contains a Machine Learning Microservice, that has been trained to predict housing prices in Boston. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This repository has been operationalized to :

- `run_docker.sh` : Deploy containerized application using Docker and make a prediction `make_prediction.sh`
- `upload_docker.sh`: Upload container to Docker Hub.
- `run_kubernetes.sh` : Run the deployed application in a Kubernetes cluster and make a prediction `make_prediction.sh`
- `.circleci/config.yml`: Integrate with CircleCI to indicate code has been tested

---
## HOW TO START

**Pre-Requisites**: Python 3.7, Docker Desktop, Minikube

After Forking/Cloning, you can get up and running in just a few minutes. From the project's root folder:

1. **Setup the Environment**
  
  Create a virtualenv and activate it
   ```
   python3 -m venv <your_venv>
   source <your_venv>/bin/activate
   ```

2. **Install dependencies**

  Run `make install` to install the necessary dependencies


3. **Run app.py**

* Standalone:  `python app.py`
* Run in Docker:  `./run_docker.sh` + `make_prediction.sh`
* Run in Kubernetes:  `./run_kubernetes.sh` + `make_prediction.sh`
