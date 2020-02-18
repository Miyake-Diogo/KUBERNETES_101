# Overview dos comandos básicos do kubernetes


## kubectl get nodes
verifica se todos os nodes do nosso cluster estão ok:

![](images/kubernetes_9.png)

## source <(kubectl completion bash)
Permite usar o auto-complete: 

![](images/kubernetes_10.png)



## kubectl describe node {nome do node}
Verifica os detalhes do node:

![](images/kubernetes_11.png)
![](images/kubernetes_12.png)

## kubectl get pods -n kube-system
Verifica os pods do namespace do kubernetes, o kube-system:

![](images/kubernetes_13.png)

## kubectl  describe pod kube-apiserver-{nodenode} -n kube-system
Usando o describe para ver detalhes de algum pod:

![](images/kubernetes_14.png)

![](images/kubernetes_15.png)



## kubectl get pods -n kube-system -o wide
Verificando os pods do namespace do kubernetes, o kube-system e utilizando a opção -o wide:

![](images/kubernetes_16.png)
![](images/kubernetes_17.png)

## kubectl run meu-nginx --image nginx
Cria um deployment do nginx.

## kubectl get deployments
Verificando o deployment criado:

![](images/kubernetes_18.png)


## kubectl describe deployment nginx
Verificando os detalhes de nosso deployment:

![](images/kubernetes_19.png)

## kubectl get pod,deployments
Uso do get pod e o get deployment juntos:

![](images/kubernetes_20.png)

## kubectl describe deployment nginx
Verificando os detalhes de nosso deployment.

## kubectl scale deployment nginx --replicas=10
Aumentando a quantidade de replicas de nosso deployment.  

## kubectl delete deployment meu-nginx
Removendo nosso deployment:
![](images/kubernetes_21.png)

## kubectl get pods --all-namespaces
Verificando os pods de todos os namespaces:
![](images/kubernetes_22.png)

## Referências 
* [Descomplicando o Kubernetes 03](https://www.linuxtips.io/post/descomplicando-o-kubernetes-03)

____
