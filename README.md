# Projeto DevOps - Grupo2

Alunas: 
- Mariana Cardozo
- Paula Feijó 
- Andrezza Almeida
- Cintia Fumi

## Objetivo do projeto: 

Criar infraestrutura em VPC na AWS e construir pipeline para app NodeJS digitalhouse-devops-app.

## Pre-requisitos de ambiente para execucao do projeto (desktop):

```
- Linux com Ansible
- Docker
- Jenkins
- Git (na versao mais recente)
```

### Passo a passo do projeto: 

1. Criar um arquivo de senha:

```
echo "SuaSenha" > ~/.ansible/.vault_pass
```

2. Dentro da pasta playbooks/vars/ criar arquivo de credenciais: 

```
ansible-vault create aws_credentials.yml
(No formato AWSAccessKeyId: ***** AWSSecretKey: *****)
```

3. Executar playbooks:

```
ansible-playbook playbooks/aws_provisioning_infra.yml
ansible-playbook playbooks/config-ansible.yml
ansible-playbook playbooks/docker.yml
ansible-playbook  playbooks/jenkins.yml

```