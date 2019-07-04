# README-GuiaInstalacao-GCloud-Docker-NGINX.md


## 1. Introdução

O objetivo deste guia de configuração é **Instalar** e executar uma imagem **Docker** do servidor HTTP **NGINX** no Google Cloud Engine **GCloud** . 


### 2. Premissas

* [Google Cloud Plataform - GCloud](https://cloud.google.com/)


### 3. Passo-a-passo

### 3.1. Criação de uma instância Linux no GCloud

```cloudshell
gcloud compute firewall-rules create allow-http \
  --target-tags http-servers \
  --allow tcp:80

gcloud beta compute instances create-with-container nginx-vm \
  --tags http-servers \
  --container-image nginx:alpine
  --zone us-east1-a
```

## Referências ##

* [GCloud Quick Start](https://cloud.google.com/compute/docs/quickstart-linux)
* [Instância do GCloud](https://cloud.google.com/compute/docs/instances/?hl=pt-br)
* [Create a Linux VM on Google Cloud Platform (GCP)](https://www.youtube.com/watch?v=2d5LzJNj46w)
* [Google Cloud Plataform - GCloud](https://cloud.google.com/)
* [Vídeo Deploy Containeger Google Cloud Engine](https://www.youtube.com/watch?v=wKiW1nufh1k)
* [Tutorial create GCloud Kubernets](https://cloud.google.com/kubernetes-engine/docs/tutorials/hello-app)
