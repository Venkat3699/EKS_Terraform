# EKS-Terraform

#### AWSCLI
```
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
    sudo apt install unzip
    unzip awscliv2.zip
    sudo ./aws/install
```

#### Terraform
```
    sudo apt-get update && sudo apt-get install -y gnupg software-properties-common

    wget -O- https://apt.releases.hashicorp.com/gpg | \
    gpg --dearmor | \
    sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null

    echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
    https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
    sudo tee /etc/apt/sources.list.d/hashicorp.list

    sudo apt update

    sudo apt-get install terraform -y

```

#### Kubectl
```
    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
    chmod +x kubectl
    sudo mv kubectl /usr/local/bin/
```

#### eksctl
```
    curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
    sudo mv /tmp/eksctl /usr/local/bin
```

#### Helm
```
	curl -LO https://get.helm.sh/helm-v3.9.0-linux-amd64.tar.gz
	tar -zxvf helm-v3.9.0-linux-amd64.tar.gz
	sudo mv linux-amd64/helm /usr/local/bin/helm
	export PATH=$PATH:/usr/local/bin
	helm version
```

#### Update KubeConfig File
```
    aws eks --region ap-south-1 update-kubeconfig --name devops-cluster
```