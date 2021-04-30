# Kubernetes

O kubernetes vem para solucionar o problema de ter muitos containers rodando em uma máquina qualquer ou seja uma hora isso vai ter um estouro de memoria e de processamento 

![img](https://caelum-online-public.s3.amazonaws.com/kubernetes/Transcri%C3%A7%C3%A3o+Externa/Imagens/aula1_video2_imagem3.PNG)

Existe a escalabilidade vertical que resolve este caso

![img2](https://caelum-online-public.s3.amazonaws.com/kubernetes/Transcri%C3%A7%C3%A3o+Externa/Imagens/aula1_video2_imagem4.PNG)

Mas o Kubernetes vem para ajudar na escalabilidade vertical e horizontal 

![img3](https://caelum-online-public.s3.amazonaws.com/kubernetes/Transcri%C3%A7%C3%A3o+Externa/Imagens/aula1_video2_imagem5.PNG)

Caso alguma maquina pare o kubernetes sobe uma nova maquina, caso ocorra de acontecer estouro de mémoria o kubernetes é capaz de lidar com isso.

Então a questão é essa: o Kubernetes é capaz de criar e gerenciar um cluster para que nós consigamos manter a nossa aplicação escalável sempre que nós quisermos adicionar novos containers, sempre que nós quisermos reiniciar a nossa aplicação de maneira automática, caso ela tenha falhado. Então nós chamamos isso de orquestração de containers.

Ícone do Kubernetes conectado à área de cluster passando por AWS, Google Cloud e Azure. Nesta área, há três máquinas com um container acima cada, sendo que apenas dois apresentam medidores no valor máximo.

Então o Kubernetes é um orquestrador de containers capaz de resolver todos esses problemas que eu listei para vocês.

### Como funciona a API que controla todo o ambiente do Kubernetes

![image](https://user-images.githubusercontent.com/48387196/116601254-ac418000-a900-11eb-9bbf-62001c345858.png)

os pods são os containers, iguais os do docker e eu posso colocar dois container em um pod.

### Criar nosso cluster virtualizado

```
minikube start --vm-driver=virtualbox
```

Assim estamos criando um cluster dentro da máquina virtual que o VB vai criar.

### Comands 

Subir um pod com uma imagem 

```
kubectl run features --image=features
```

Ver se o pod já subiu

```
kubectl get pods 
```

Ver em tempo real

```
kubectl get pods --watch
```

Ver tudo que ocorreu dentro do pod

```
kubectl describe pod features
```

Ver os pods de forma wide com todas as informações:

```
kubectl get pods -o wide
```

Deletar um pod 

``` 
kubectl delete pod <nomedopod>
```
```
kubectl delete -f arquivo.yaml
```
