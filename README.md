# mlflow-test

# for dagshub

MLFLOW_TRACKING_URI=https://dagshub.com/hbbolaji/mlflow-test.mlflow \
MLFLOW_TRACKING_USERNAME=hbbolaji \
MLFLOW_TRACKING_PASSWORD=4bdb5a1658312cbc56f3d871f4a979d11754c578 \
python script.py

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/hbbolaji/mlflow-test.mlflow
export MLFLOW_TRACKING_USERNAME=hbbolaji
export MLFLOW_TRACKING_PASSWORD=4bdb5a1658312cbc56f3d871f4a979d11754c578
```

# MLflow on AWS

# MLflow on AWS setup

1. Login to AWS console
2. Create IAM user with Administration Access
3. Export the credential in your AWS cli by running "aws configure"
4. Create a s3 buckent
5. Create EC2 machine (Ubuntu) & and add security groups 5000 port

Run the following command on EC2 machine

```bash
sudo apt update

supo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure

## Finally
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-bucket23


# set uri on local terminal and in your code

export MLFLOW_TRACKING_URI=http://ec2-51-21-134-52.eu-north-1.compute.amazonaws.com/
```
