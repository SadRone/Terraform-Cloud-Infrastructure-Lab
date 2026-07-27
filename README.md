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
