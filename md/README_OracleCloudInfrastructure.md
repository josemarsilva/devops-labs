`devops-labs/doc/README_OracleCloudInfrastructure.md` - Template Git Project

## 1. Introdução

Este repositório contém as documentações e os artefatos do laboratório com  **Oracle Cloud Infraestructure**.

* Tabela de Conteúdo
  * Introdução
  * Documentação
    * Diagrama de Caso de Uso (Use Case Diagram)
    * Diagrama de Implantação (Deploy Diagram)
    * Diagrama de BPMN (Business Process Modeling Notation)
    * Diagrama de Mapa Mental (Mind Map Diagram)
    * Estratégia de Branches (Branch Strategy Workflow)
    * Diagrama de Pacotes Classes (Packages and Class Class Diagram)
    * Diagrama de Sequencia (Sequence Diagram)
    * Notas de atenção e Avisos
    * Glossário de Termos (Glossary)
  * Projeto
    * Pré-Requisitos, Pré-Condições e Premissas
    * Guia do Desenvolvedor e Administrador
    * Guia de Implantação, Configuração e Instalação
    * Guia de Execução, Demonstração e Cenários de Teste
	* Guia de Estudo
    * Design Patterns, Standard, Conventions and Best Practices
  * I - Referências


## 2. Documentação

### 2.1. Diagrama de Caso de Uso (Use Case Diagram)

![UseCaseDiagram-Context.png](./doc/uml-diagrams/UseCaseDiagram-Context.png) 


### 2.2. Diagrama de Implantação (Deploy Diagram)

![DeployDiagram-Context.png](./doc/uml-diagrams/DeployDiagram-Context.png) 


### 2.3. Diagrama de BPMN (Business Process Modeling Notation)

![BpmnDiagram-Context.png](./doc/bpmn-diagrams/BpmnDiagram-Context.png) 


### 2.4. Diagrama de Mapa Mental (Mind Map Diagram)

![MindMapDiagram-Context.png](./doc/mind-maps/MindMapDiagram-Context.png) 


### 2.5. Estratégia de Branches (Branch Strategy Workflow)

Sugestão de [estratégia de branches e workflow](https://github.com/josemarsilva/eval-git#38-estrat%C3%A9gia-de-gerenciamento-de-branches) :
* `master`: pronto para produção
* `develop`: último desenvolvimento pronto para produção


### 2.6. Diagrama de Pacotes Classes (Packages and Class Class Diagram)

![ClassDiagram-Context.png](./doc/uml-diagrams/ClassDiagram-Context.png) 


### 2.7. Diagrama de Sequencia (Sequence Diagram)

![SequenceDiagram-Context.png](./doc/uml-diagrams/SequenceDiagram.png) 


### 2.8. Notas de atenção e Avisos (Notice and information)

*  n/a


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
