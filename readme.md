EKS deploy

eksctl create cluster --config-file eks.yml

eksctl delete cluster --config-file eks.yml

deploy:
kubectl apply -f <filename>

to check running pods
kubectl get pods -A

EBS or EFS static
=================
1. Install drivers
2. Give permissions in EC2 role
3. create volume
4. create PV(physical representation of volume)
5. create PVC
6. volume mount to pod

if EBS volume should be in the same az as in instance
if EFS SG should allow port 2049

EBS of EFS dynamic
=================
1. Install drivers
2. Give permissions in EC2 role
3. create storage class
4. create PVC with SC name, volume and PV will be created automatically
5. volume mount to pod

in case of dynamic pod pvc creates volume, so it creates in the same az where ec2 instance is there
if EFS SG should allow port 2049