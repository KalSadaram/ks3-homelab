# Light-weight CI/CD k3s Implementation
k3s-homelab
Managing Home Infra with GitOps [MicroK8S, Helm releases with Flux Help Operator]

# GOAL
* Single Cluster on Intel Nuc ✅
* Ansible for inital setup ✅
* Flux & Help Operator Setup

Start Over :-)

# Step 1 - Setup-up Ansible

# ![Ref](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#prerequisites)

sudo apt update

sudo apt install software-properties-common

sudo apt-add-repository --yes --update ppa:ansible/ansible

sudo apt install ansible


# Step 2 - Run Ansible playbook check

## Set Ansible configuration

navigate to ansible folder
ex: cd /ansible

### Set configuration
export ANSIBLE_CONFIG=ansible.cfg

### check ansible config
sudo ansible --version

sudo ansible-playbook main.yml --check


sudo ansible-playbook main.yml -i inventory/hosts.ini -kK --check

SSH password: = k
BECOME password = -K

# Inspired by below repo's
![https://github.com/rancher/k3s-ansible](https://github.com/rancher/k3s-ansible)

![https://github.com/onedr0p/k3s-gitops](https://github.com/onedr0p/k3s-gitops)


