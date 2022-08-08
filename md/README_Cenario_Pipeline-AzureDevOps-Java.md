`./md/README_Cenario_Pipeline-AzureDevOps-Java.md` - Pipeline Java on Azure DevOps

## 1. Introdução

Este repositório contém os artefatos do projeto / laboratório **LAB-XX: Pipeline de Java on Azure DevOps** abaixo do projeto [devp´s=çabs](../README.md). Este laboratório consiste em:
* Configurar o DevOps Azure para o Pipeline
* Explorar os recursos e funcionalidades básicas do produto

##### Table of Contents  
- [1. Introdução](#1-introdução)
- [2. Documentação](#2-documentação)
- [3. Projeto / Laboratório](#3-projeto--laboratório)
  * [3.1. Pré-Requisitos, Pré-Condições e Premissas](#31-pré-requisitos-pré-condições-e-premissas)
    + [3.1.1. Tecnologias e ferramentas](#311-tecnologias-e-ferramentas)
    + [3.1.2. Ferramental de apoio](#312-ferramental-de-apoio)
  * [3.2. Guia do Desenvolvedor e Administrador](#32-guia-do-desenvolvedor-e-administrador)
  * [3.3. Guia de Implantação, Configuração e Instalação](#33-guia-de-implantação-configuração-e-instalação)
  * [3.4. Guia de Demonstração e Teste](#34-guia-de-demonstração-e-teste)
  * [3.5. Guia de Estudo](#35-guia-de-estudo)
- [I - Referências](#i---referências)



## 2. Documentação

* n/a


## 3. Projeto / Laboratório

### 3.1. Pré-Requisitos, Pré-Condições e Premissas

#### 3.1.1. Tecnologias e ferramentas

* Programming Languages / Libraries / IDE:
	* Java JDK 1.8 / Eclipse (version Neon recommended) / Apache Maven 3.6 (recommended > 3.3)
* Azure DevOps: Pipeline

#### 3.1.2. Ferramental de apoio

* Ferramenta: [Draw.IO](https://app.diagrams.net/) (only for diagrams design and documentation)
* Ferramenta: [FreeMind for Windows](https://freemind.br.uptodown.com/windows)


### 3.3. Guia de Implantação, Configuração e Instalação

* n/a


### 3.2. Guia do Desenvolvedor e Administrador

* n/a


### 3.3. Guia de Implantação, Configuração e Instalação

* n/a


### 3.4. Guia de Demonstração e Teste

* n/a


### 3.5. Guia de Estudo

### 3.5.1. Documentação oficial e tutoriais de referência

* n/a

### 3.5.2. Pré-Requisitos

* Conta `MyAzureAccount` no serviço da [Azure DevOps](https://dev.azure.com/)

![Azure DevOps - Home Page](images/azure-devops-pipeline-01.png)

### 3.5.3. Criar uma nova `Organization` no Azure DevOps

* Em `https://dev.azure.com/MyAzureAccount/` clique no menu lateral esquerdo `New Organization`

![Azure DevOps - New Organization](images/azure-devops-pipeline-02.png)

* Em dialogbox `Azure DevOps - Get started with Azure DevOps` clique botão `Continue`
* Em dialogbox `Azure DevOps - Almost done ...` preencha os campos:
  * Name your Organization: `MyLabAzureOrg` (substituir por outro nome único se conflitar)
  * We will host your project in: `Brazil`
  * Fill capcha and clique `Continue`

![Azure DevOps - New Organization](images/azure-devops-pipeline-03.png)

### 3.5.4. Criar um novo `Project` no Azure DevOps

* Em `https://dev.azure.com/MyLabAzureOrg/` clique no botão sobre o link no menu lateral esquerdo `New Project`

![Azure DevOps - New Project](images/azure-devops-pipeline-04.png)

* Em formulário `Create a project to get started` preencha os campos:
  * Project Name: `MyLabProject-01`
  * Description: `MyLabProject-01`
  * Visibility: `Provate`
  * Advanced - Version Control: `Git`
  * Advanced - Work item Process: `Basic`


### 3.5.5. Executar _Run_ o `Pipeline` no Azure DevOps


## I - Referências

* Github README.md writing sintax
  * [Basic Github Markdown Writing Format](https://docs.github.com/pt/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax)  
  * [Github Markdown Chead Sheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)
  * [Github Mastering Markdown](https://guides.github.com/features/mastering-markdown/#what)
  * [Table of contents generated with markdown-toc](http://ecotrust-canada.github.io/markdown-toc/)

