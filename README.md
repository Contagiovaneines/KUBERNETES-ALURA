# KUBERNETES-ALURA
Explore o Kubernetes e aprenda a gerenciar contêineres. Crie Pods, exponha serviços, configure volumes e probes de saúde, e dimensione horizontalmente. Com exemplos práticos e comandos Linux.
---

# Curso de Containers com Kubernetes

Neste curso, aprendemos sobre os fundamentos dos containers e como gerenciá-los usando Kubernetes. Abaixo está um resumo dos tópicos abordados e das habilidades adquiridas, com exemplos práticos e comandos para aplicá-los no Linux.

## Arquitetura Kubernetes

Kubernetes é uma plataforma de código aberto para automatizar a implantação, o dimensionamento e a gestão de aplicações em contêineres. Ele utiliza uma arquitetura cliente-servidor composta por vários componentes principais, incluindo o Master Node, que coordena todas as operações no cluster, e os Worker Nodes, onde os contêineres são executados.

Exemplo de comando no Linux para verificar os componentes do cluster Kubernetes:
```bash
kubectl get nodes
kubectl get pods --all-namespaces
```

## Gerenciamento de Contêineres com Kubernetes

Aprendemos como o Kubernetes gerencia os contêineres, usando o kubelet para monitorar a saúde dos contêineres e o kube-proxy para lidar com o tráfego de rede para os contêineres.

Exemplo de comando no Linux para verificar os logs de um contêiner:
```bash
kubectl logs <pod_name>
```

## Uso de Pods com kubectl

Os Pods são a unidade mais básica no Kubernetes, consistindo em um ou mais contêineres que compartilham armazenamento e rede. Aprendemos a criar e gerenciar Pods usando o kubectl, a ferramenta de linha de comando do Kubernetes.

Exemplo de comando no Linux para criar um Pod:
```bash
kubectl apply -f pod.yaml
```

## Tipos de Serviço e Exposição de Pods

Exploramos os diferentes tipos de serviços no Kubernetes, como ClusterIP, NodePort e LoadBalancer, e como usar esses serviços para expor os Pods para dentro e fora do cluster.

Exemplo de comando no Linux para expor um serviço:
```bash
kubectl expose deployment my-deployment --type=NodePort --port=8080
```

## Variáveis de Ambiente com ConfigMaps

Aprendemos a definir variáveis de ambiente para nossos contêineres usando ConfigMaps, que são objetos Kubernetes que fornecem uma maneira de armazenar dados de configuração.

Exemplo de comando no Linux para criar um ConfigMap:
```bash
kubectl create configmap my-config --from-literal=key1=value1 --from-literal=key2=value2
```

## ReplicaSets e Deployments

Discutimos o uso de ReplicaSets e Deployments para garantir a alta disponibilidade e escalabilidade das nossas aplicações.

Exemplo de comando no Linux para criar um Deployment:
```bash
kubectl create deployment my-deployment --image=my-image:latest
```

## Tipos de Volumes e Storage Classes

Exploramos os diferentes tipos de volumes no Kubernetes, como emptyDir, hostPath e persistentVolumeClaim, e como usar Storage Classes para criar volumes dinamicamente.

Exemplo de comando no Linux para criar um PersistentVolumeClaim:
```bash
kubectl apply -f pvc.yaml
```

## Utilização do StatefulSet

Aprendemos sobre StatefulSets, que são usados para aplicações que requerem identidade persistente e garantias de rede únicas para cada instância, como bancos de dados.

Exemplo de comando no Linux para criar um StatefulSet:
```bash
kubectl apply -f statefulset.yaml
```

## Liveness e Readiness Probes

Discutimos a importância das Liveness e Readiness Probes para garantir a disponibilidade e a saúde dos nossos contêineres.

Exemplo de comando no Linux para definir uma Liveness Probe:
```bash
kubectl apply -f liveness_probe.yaml
```

## Escalabilidade Horizontal com Horizontal Pod Autoscaler

Aprendemos a escalar automaticamente os nossos Pods horizontalmente com o Horizontal Pod Autoscaler.

Exemplo de comando no Linux para habilitar o Horizontal Pod Autoscaler:
```bash
kubectl autoscale deployment my-deployment --min=2 --max=5 --cpu-percent=80
```

Espero que este resumo ajude a entender os conceitos abordados neste curso. Sinta-se à vontade para explorar mais a fundo cada tópico conforme necessário. Se tiver alguma dúvida ou precisar de mais informações, não hesite em entrar em contato!

--- 
