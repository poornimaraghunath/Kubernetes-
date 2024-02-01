# Eks is a managed control plane it provides Highly avaialble kubernetes cluster and the data plane managed bys us.

In data plane two type of resources can be used that is
  1. AWs Ec2 machines
  2. AWS fargate( they are aws severless compute they are similar to aws lambda but can be used for running containers)

  By using EKS control plane and AWS fargate we can build the robust infrastructure on AWS

  # Kubernetes can installed be on EC2 using kubeadm or kops 

  # In this project will learn how to create a kubernetes cluster on EKS and deploy the application to that

  When the applications are deployed as pods they can be used only within the cluster but to access the application from outside we need to create the service

  # There are 3 types of services
     
     1. cluster Ip - in these applications can be accessed only in the cluster
     2. Nodeport  - In these applications can be accessed only at node level
     3. loadbalancer - In these applications can be acecssed from outside but we need to provide elastic ip address for all the resources which will cost more in order to avoid that will use the ingress method

     For that we need to deploy ingress controller in the cluster all the loadbalancers like nginx ,F5 they have there own ingress controllers as soons as ingress resource is deployed they will create ALB environment in public subnet which will allow the users to access the application.