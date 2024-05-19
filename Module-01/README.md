# 📋 Module 1: Intro & Environment Setup

When you are designing a machine learning system, your job doesn't end with building the model—and achieving a high accuracy score and a low validation error! For the model to be actually helpful—you will have to consider deploying it, and also ensure that the model's performance does not degrade over time. And MLOps is a set of *best practices* for putting machine learning models into production.

![image](https://user-images.githubusercontent.com/47279635/168582280-52820583-d0bb-4b46-add4-b2fa4c09bc1b.png)

## 🎯 Steps in a Machine Learning Project
The various stages in a machine learning project can be broadly captured in the following three steps:
1. **Design**: In the `design` step, you are considering the problem at hand—to decide whether or not you'll need a machine learning algorithm to achieve the objective. 
2. **Train**: Once you decide on using a machine learning algorithm, you `train` the model and optimize its performance on the validation dataset.
3. **Operate**: The `operate` state captures the performance of the model after it's deployed. Some of the questions that you'll answer throughout the course, include:
  - If the performance of the model degrades, can you retrain the model in a cost-effective manner?
  - How do you ensure that the deployed model performs as expected—that is, how do you monitor the model's performance in production?
  - What are the challenges associated with monitoring ML models?

## ⚙ Environment Setup

Recommended development environment: Linux

### 1. Download and install the Anaconda distribution of Python
```sh
$ wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh

```

### 2. Update existing packages
```sh
$ sudo apt update
```
### 3. Install Docker
```sh
$ sudo apt install docker.io
```

### 4. Install Docker Compose

4.1 Install docker-compose in a separate directory
```sh
$ mkdir soft
$ cd soft
```

4.2 To get the latest release of Docker Compose, go to https://github.com/docker/compose and download the release for your OS.

```sh
$ wget https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-linux-x86_64 -O docker-compose
```
4.3 Make it executable
```sh
$ chmod +x docker-compose
```
4.4 Add to path
```sh
$ nano .bashrc
# In .bashrc, add:
export PATH="${HOME}/soft:${PATH}"
# Run
$ source .bashrc
```

### [Optional] Run Docker without `sudo`
```sh
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
```
### 5. Run Docker
```sh
$ docker run hello-world
```

## ⚙ Dataset

## 1.1 What is MLOps

**MLOps**, short for Machine Learning Operations, refers to the practices, methodologies, and tools used to streamline and operationalize the lifecycle of machine learning (ML) models. It aims to bridge the gap between data scientists, who develop and train models, and production environments, where models are deployed and maintained.

Traditionally, the development and deployment of ML models have been treated as separate stages, leading to challenges when transitioning from experimentation to production. MLOps seeks to address these challenges by introducing a set of best practices for managing ML workflows, collaboration, and automation.

Here are some key components and concepts associated with MLOps:

**Version control**: Applying version control systems (e.g., Git) to ML models, code, and data, enabling easy tracking of changes and reproducibility.

**Automation and orchestration**: Using automation tools to streamline repetitive tasks, such as data preprocessing, model training, evaluation, and deployment. Orchestration frameworks, like Kubeflow or Apache Airflow, help manage complex workflows.

**Continuous Integration and Continuous Deployment (CI/CD)**: Adapting CI/CD principles from software development to ML, allowing for frequent and automated model updates and deployments.

**Infrastructure and environment management**: Utilizing tools like Docker and Kubernetes to containerize ML models and manage scalable and reproducible environments across different stages, from development to production.

**Model monitoring and management**: Implementing monitoring solutions to track model performance, detect anomalies, and ensure models remain effective over time. This includes logging relevant metrics and retraining models when necessary.

**Collaboration and reproducibility**: Establishing practices for sharing code, data, and experiment results, enabling collaboration among data scientists and ensuring reproducibility of ML workflows.

**Governance and compliance**: Addressing ethical and legal considerations, such as data privacy, bias mitigation, and regulatory compliance, throughout the ML lifecycle.

By adopting MLOps practices, organizations can enhance the efficiency, scalability, and reliability of their ML deployments. It promotes a systematic approach to managing ML models, accelerates time to market, and facilitates collaboration between different stakeholders involved in ML development and deployment.

## 1.2 Environment preparation


### Step 1
Download and install the Anaconda distribution of Python
```
wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh
bash Anaconda3-2022.05-Linux-x86_64.sh
```
### Step 2
Update existing packages
```
sudo apt update
```
### Step 3
Install Docker
```
sudo apt install docker.io
```
### Step 4
Create a separate directory for the installation
```
mkdir soft
cd soft
```
To get the latest release of Docker Compose, go to https://github.com/docker/compose and download the release for your OS.
```
wget https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64 -O docker-compose
```
Make it executable
```
chmod +x docker-compose
```
Add to the soft directory to PATH. Open the .bashrc file with nano:
```
nano ~/.bashrc
```
In .bashrc, add the following line:
```
export PATH="${HOME}/soft:${PATH}"
```

nano.PNG
Save it using ctrl + O , hit enter at the File Name to Write prompt, and then exit using ctrl + Z

Run the following to make sure the changes are applied:
```
source ~/.bashrc
```
### Step 5
Run Docker
```
docker run hello-world
```
