# Terraform-Cloud-Infrastructure-Lab
A zero-cost infrastructure-as-code lab demonstrating Terraform, Docker networking, secure AWS architecture design, monitoring, infrastructure testing, and incident remediation.


Install **Terraform** must be done through HashiCorp [ Official Storage ] - for safety purposes:
{

sudo apt-get update && \
sudo apt-get install -y gnupg software-properties-common wget lsb-release

wget -O- https://apt.releases.hashicorp.com/gpg | \
gpg --dearmor | \
sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(grep -oP '(?<=UBUNTU_CODENAME=).*' /etc/os-release || lsb_release -cs) main" | \
sudo tee /etc/apt/sources.list.d/hashicorp.list

sudo apt-get update
sudo apt-get install -y terraform

}

After the installation process:

{

cd ~/projects
→ 프로젝트들을 보관하는 상위 폴더로 이동

mkdir -p terraform-cloud-infrastructure-lab
→ 새 프로젝트 폴더 생성

cd terraform-cloud-infrastructure-lab
→ 새 프로젝트 안으로 이동

git init
→ 이 폴더를 Git 저장소로 만듦

git branch -M main
→ 기본 브랜치 이름을 main으로 설정

pwd
→ 현재 위치 확인

ls -la
→ 숨겨진 .git 폴더까지 확인

}

Another Clear Steps:

{

git remote add origin ...
→ 현재 Ubuntu 폴더를 GitHub 저장소와 연결

git pull origin main
→ GitHub에 있는 README를 Ubuntu로 내려받음

ls -la
→ README가 내려왔는지 확인

}

***Error*** 
-> curl: (28) Connection timed out after 15001 milliseconds

Solution: Exit Ubuntu, and reopen through Terminal. Then, connect to GIT after finding the path with cd.
-> curl -I --http1.1 --max-time 15 https://github.com

***Finalize Terraform Basic Set Up***

{

mkdir -p local-docker-infrastructure aws-production-design/modules security monitoring incidents docs scripts .github/workflows

find . -maxdepth 2 -type d | sort

printf ".terraform/\n*.tfstate\n*.tfstate.*\n*.tfplan\ncrash.log\ncrash.*.log\n*.tfvars\n!*.tfvars.example\n.env\n" > .gitignore

}

_________________________________________________________________________________________________________________________________

***Terraform Folder***
cd local-docker-infrastructure

pwd

nano versions.tf
[
terraform {
  required_version = ">= 1.5.0"

  required_providers {
    docker = {
      source  = "kreuzwerker/docker"
      version = "~> 3.0"
    }
  }
}
]

Then, press: Ctrl O -> Enter -> Ctrl X [ to save the above terraform script ]

cat versions.t

git status --short

Check for the processes using the above code


















cat .gitignore

git status --short

}
