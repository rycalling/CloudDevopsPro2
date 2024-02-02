# CD12352 - Infrastructure as Code Project Solution
# Rahul Yadav
This repository contains the code created by Rahul Yadav for the final project of course 2 Infrastructure as Code in the Cloud DevOps Engineer Nanodegree.

## Spin up instructions
Ran the AWS CLI and configured the user with details available from IAM User
 Created the network infrastructure

# Create Infrastructure for UdaGram
Ran the AWS CLI and configured the user with details available from IAM User
 Created the network infrastructure

./createNetwork.sh or
aws cloudformation create-stack --stack-name projectUdagramRahulInfra --template-body file://network.yml --parameters file://network-parameters.json --region us-east-2 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"

# Create Application UdaGram

./createUdagram.sh or

aws cloudformation create-stack --stack-name projectUdagramRahulApp --template-body file://udagram.yml --parameters file://udagram-parameters.json --region us-east-2 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"

## Tear down instructions
/delete.sh <stack name> <region name> or
aws cloudformation delete-stack --stack-name <stack name> --region=<region name>