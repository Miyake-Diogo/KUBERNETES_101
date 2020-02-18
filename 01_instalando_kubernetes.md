# Instalação do Kubernetes

Para começar a aprender Kubernetes é necessário o entendimento básico de Docker pelo menos. 

[Para acessar o tutorial básico.](https://github.com/Miyake-Diogo/DOCKER_101)  

Obs.: Estarei colocando somente os comando para instalção no Linux, para o windows ou mac veja no link de referências.

Antes é necessário ter uma maquina virtual como background (vmware/virtualbox, etc)
Antes de Instalar o Minikube que é a ferramenta que usaremos para orquestrar os containers com o Kubernetes, estaremos instalando o KUBECTL.  

## KUBECTL

A ferramenta de linha de comando Kubernetes, kubectl, permite executar comandos nos clusters Kubernetes. Você pode usar o kubectl para implantar aplicativos, inspecionar e gerenciar recursos de cluster e visualizar logs. Para obter uma lista completa das operações do kubectl, [consulte Visão geral do kubectl.](https://kubernetes.io/docs/reference/kubectl/overview/)  

Para isso Use o comando na linha de comando: 

```
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl  

```

Depois de as permissões na pasta: 

```
chmod +x kubectl && mv kubectl /usr/local/bin/
```

## MINIKUBE
O Minikube é uma ferramenta que facilita a execução local do Kubernetes. O Minikube executa um cluster Kubernetes de nó único dentro de uma Máquina Virtual (VM) no seu laptop para usuários que desejam experimentar o Kubernetes ou desenvolvê-lo diariamente.  

Agora instalaremos o MINIKUBE.

```
curl -Lo minikube https://github.com/kubernetes/minikube/releases/download/v0.28.0/minikube-linux-amd64
```
Depois de as permissões na pasta:
```
chmod +x minikube && mv minikube /usr/local/bin/
```

Agora iniciemos o MINIKUBE com o docker como driver, com o Comando:

```
minikube start --vm-driver=none
```
Para ver o status:
```
minikube status
```

E para vermos os nodes:

```
kubectl get nodes
```

Para parar o serviço do minikube:
```
minikube stop
```

## Referências

* [Descomplicando o Kubernetes 01](https://www.linuxtips.io/post/descomplicando-o-kubernetes-01)
* [Install KUBECTL on linux](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-linux)
* [Install Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/)