# kops-generating-file
generates kops file and than terraform apply 

Prerequisities are:
terraform 0.11.15
wget https://releases.hashicorp.com/terraform/0.11.15-oci/terraform_0.11.15-oci_linux_amd64.zip


kubectl   1.15
curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.0/bin/linux/amd64/kubectl
chmod +x ./kubectl
Move the binary in to your PATH.
sudo mv ./kubectl /usr/local/bin/kubectl
kubectl version 


kops      1.15




kops create cluster olgaojjeh.com --state=s3://olgaojjeh.com --node-count=3 --zones="eu-west-1a,eu-west-1b,eu-west-1c" --node-size="t2.micro" --master-size="t2.micro" --master-zones="eu-west-1a,eu-west-1b,eu-west-1c" --networking="weave" --topology="private" --bastion="true" --out=. --target="terraform" 
