`devops-labs/doc/README_INFRA-OracleCloudInfrastructure.md` - Evaluation Oracle Cloud

## 1. Introdução

Este repositório contém as documentações e os artefatos do laboratório com  **Oracle Cloud Infraestructure**.

## 2. Documentação

### 2.2. Diagrama de Implantação (Deploy Diagram)

![DeployDiagram-Context.png](./doc/uml-diagrams/DeployDiagram-Context.png) 


### 2.5. Estratégia de Branches (Branch Strategy Workflow)

Sugestão de [estratégia de branches e workflow](https://github.com/josemarsilva/eval-git#38-estrat%C3%A9gia-de-gerenciamento-de-branches) :
* `master`: pronto para produção
* `develop`: último desenvolvimento pronto para produção


### 2.9. Glossário de Termos (Glossary)

De uma forma geral, vamos tentar <ins>definir</ins> e <ins>caracterizar</ins> alguns dos termos utilizados neste projeto para permitir uma melhor compreensão e entendimento:


## 3. Projeto

### 3.1. Pré-Requisitos, Pré-Condições e Premissas

#### a. Tecnologias e ferramentas

* Java JDK 1.8
* Eclipse (version Neon recommended)
* Apache Maven 3.6 (recommended > 3.3)
* NodeJS (Development, Build and Deploy)
* JMeter
* SOAP UI (apenas para sanidade e comparativo)
* Postman (apenas para sanidade e comparativo)
* Curl(Window e Linux - apenas para sanidade e comparativo)
* Docker or Kubernetes or VirtualBox or On-Premisse infrastructure (Deployment Infraestructure)
* Cloud infrastructure: AWS or GPC or Azure
* Python 3.x (3.8 recommended)
* Venv


#### b. Ferramental de apoio

* Ferramenta: [Draw.IO](https://app.diagrams.net/) (only for diagrams design and documentation)


### 3.2. Guia do Desenvolvedor e Administrador

* Faça um clone do projeto `git clone`. Use o _branch_ `master` se o _branch_ `develop` não estiver disponível
* Leia as documentações disponíves em "2. Documentação"  and "3.x. Design Patterns, Standard, Conventions and Best Practices"


### 3.3. Guia de Implantação, Configuração e Instalação

#### a. Instalando/Clonando este repositório no ambiente

* Windows

```cmd
C:\> md githome
C:\> cd githome
C:\githome> git clone https://github.com/josemarsilva/apm-labs.git
```

* Linux

```sh
$ sudo mkdir /opt
$ sudo mkdir /opt/githome
$ sudo chown -R $USER:$USER /opt/githome
$ cd /opt/githome
$ git clone https://github.com/josemarsilva/apm-labs.git
```


#### b. Instalando NodeJS (em Linux Ubuntu)

* https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server#31-nodejs


#### c. Instalando Docker e Docker Composer (em Linux Ubuntu)

* https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server/blob/master/README.md#41-docker---installation
* https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server/blob/master/README.md#42-docker-composer---installation


#### d. Instalando JMeter

* Localize a última versão de distribuição do _Binaries_ do JMeter em https://jmeter.apache.org/download_jmeter.cgi

```sh
$ sudo mkdir /opt
$ cd /opt
$ wget https://downloads.apache.org//jmeter/binaries/apache-jmeter-5.3.tgz
$ tar -xvf apache-jmeter-5.3.tgz
$ sudo chown -R $USER:$USER /opt/apache-jmeter-5.3
$ rm apache-jmeter-5.3.tgz
```


### 3.4. Guia de Demonstração e Teste

* n/a


### 3.5. Guia de Estudo

* n/a

#### 3.5.1. Patterns, Standard, Conventions and Best Practices

* Diagrama de Sequencia - Synchronous Request / Response

![SequenceDiagram-Context-SynchronousRequestResponse.png](./doc/uml-diagrams/SequenceDiagram-Context-SynchronousRequestResponse.png) 

* Diagrama de Sequencia - Synchronous Request / Acknowledge

![SequenceDiagram-Context-SynchronousRequestAcknowledge.png](./doc/uml-diagrams/SequenceDiagram-Context-SynchronousRequestAcknowledge.png) 

* Diagrama de Sequencia - Synchronous Request / Acknowledge / Poll

![SequenceDiagram-Context-SynchronousRequestAcknowledgePoll.png](./doc/uml-diagrams/SequenceDiagram-Context-SynchronousRequestAcknowledgePoll.png)

* Diagrama de Sequencia - Synchronous Request / Acknowledge / Callback

![SequenceDiagram-Context-SynchronousRequestAcknowledgeCallback.png](./doc/uml-diagrams/SequenceDiagram-Context-SynchronousRequestAcknowledgeCallback.png)

* Diagrama de Sequencia - Synchronous Request / Acknowledge / Relay / Callback

![SequenceDiagram-Context-SynchronousRequestAcknowledgeRelayCallback.png](./doc/uml-diagrams/SequenceDiagram-Context-SynchronousRequestAcknowledgeRelayCallback.png)


## I - Referências

* Github README.md writing sintax
  * [Basic Github Markdown Writing Format](https://docs.github.com/pt/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax)  
  * [Github Markdown Chead Sheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)
  * [Github Mastering Markdown](https://guides.github.com/features/mastering-markdown/#what)

00:00 início, apresentação, agenda, etc
11:00 QRCode para pedir um Trial de US$ 300,00 por 30 dias
12:00 Oracle Always Free: 1. Infraestrutura; 2. banco de dados; 3. observabilidade e gerenciamento; 4. serviços adicionais: load balancer e data-transfer
13:00 Composição média de 13 serviços: máquina virtuais, block volumes, banco de dados e monitoramento
14:30 Máquinas separadas por processador: AMD, INTEL, ARM ou AMPERE
14:45 Arquitetura Ampere até 24 GB memória RAM - viabiliza Kubernetes
17:30 Pergunta respondida: "... always free, 1 instance, shape VM.Standard.A1.Flex) 4 OCPU e 24GB RAM será sempre gratuito mesmo após o Trial de 30 dias?". Resposta: "Sim"
18:55 O que passar contabiliza 1 OCPU corresponde 2 VCPU da concorrência. A diferença é o isolamento do Core. Ideal para quem precisa de + de 4 VCPU's para seus testes
20:10 Always free: NoSQL 20 GB  + 133 mi de leituras de registros
20:50 Serviço de log da Oracle, painel escalável com 10 GB para ingestão e pesquisa de log (substitui ELK, Kibana, Grafana)
24:50 Log's criptografados em trânsito e em disco após armazenado
25:30 Always free: Ferramenta de APM gratuita na nuvem
26:30 Always free: Balanceador de carga (Load Balancer) na nuvem para você não precisar implementar com NGINX
28:45 Always free: 10 TB de data-transfer (saindo)
29:30 Always free: 36 regiões no mundo, no Brasil em Vinhedo e São Paulo. Não há diferença de custo por região
31:30 Possibilidade de integração entre nuvens da Oracle e Microsoft
33:30 Categorias de Load Balancer: de 10 MB/s até 8 GB/s. Também é possível contratar um "flex" dando mínimo e máximo.
35:10 Cloud Native and Devops: que ferramentas tem
41:05 Importante pensar em nuvem de forma agnóstica e ter opções
42:34 Login Single-Signon(SSO) após cadastro do Always Free, iniciando brincadeira e dashboard inicial
46:05 Acessando os serviços pelo menu hamburger superior esquerdo, criando uma VM instance: name, compartment(equivale a GPC Project ou AWS ResourceGroup, relaciona custos, segurança, etc), escolhendo o shape da VM = Always Free, escolhendo imagem do SO
53:50 Imagem Oracle Linux Cloud Developer - stack empacotada com diversas ferramentas desenvolvimento: Ruby, Java, Python, .Net Core, Terraform
57:30 Configurando infraestrutura de rede VCN, IP, subnet, etc
1:00:15 Configuração pode ser salva como recurso para ser gerenciado pelo Terraform ou Resource Manager (Oracle)
1:03:15 Acessando máquina criada para configurar as regras de firewall dentro da subnet. Default security list, input and output rules, ssh port, http port, etc
1:08:40 IP público precisa ser reservado, senão ele pode mudar

Referências e extra:
* [Crie sua conta Always Free e use o Oracle Cloud Infrastructure sem pagar nada por isso](https://www.youtube.com/watch?v=dMkKeEHfoNs)
* [Oracle Cloud - Instance Gratuita com 4 vCPU 24 GB RAM | Podcast DBAOCM](https://www.youtube.com/watch?v=c5VrdzBdNPA)
