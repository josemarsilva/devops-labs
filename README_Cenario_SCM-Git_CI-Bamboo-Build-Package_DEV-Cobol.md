# README - devops-labs - Cenario_SCM-Git_CI-Bamboo-Build-Package_DEV-Cobol.md

## 1. Introdução

### 1.1. Objetivo
O objetivo deste cenário é demonstrar a ferramenta de **CI**: **Bamboo** integrando com a ferramenta de **SCM**: **Github** para buscar o código fonte de um aplicativo construído em linguagem de programação **Cobol** . Em seguida o **CI** / **Bamboo** faz o **CI** / **Build** com base no **Compilador Cobol Free**, gera o **CI** / **Package** do programa objeto executável e executa um pacote de scripts de testes.

### 1.2. MindMap
![MindMap DevOps SCM-Git_CI-Bamboo-Build-Package_DEV-Cobol.png](doc/MindMap%20DevOps%20SCM-Git_CI-Bamboo-Build-Package_DEV-Cobol.png)


### 1.3. Tópicos abordados
Este cenário de laboratório aborda os seguintes tópicos, conceitos, práticas e ferramentas:

* Requirement Management - Requisito de negócio foi identificado e especificado
* SCM - Source Code GitHub.com
* Programming Language - Cobol
* CI - Continuos Integration ( Checkout Source Code, Compile, Build, Package )
* Stack Tools Used: Cobol Free/Linux, GitHub.com, Bamboo

---
## 2. Cenário

### 2.1. Diagramas 

### a. Use Case Diagram

* Diagrama de Contexto do laboratório

![UseCaseDiagram-Cenario_SCM-Git_CI-Bamboo-Build-Package_DEV-Cobol.png](doc/UseCaseDiagram-Cenario_SCM-Git_CI-Bamboo-Build-Package_DEV-Cobol.png)


### b. Deploy Diagram
![DeployDiagram-Cenario_SCM-Git_CI-Bamboo-Build-Package_DEV-Cobol.png](doc/DeployDiagram-Cenario_SCM-Git_CI-Bamboo-Build-Package_DEV-Cobol.png)



### c. BPMN
![BPMN-Cenario_DESIGN-PLAN_DEV_SCM_BUILD_PACKAGE_DEPLOY-TEST_DEPLOY-PROD.png](doc/BPMN-Cenario_DESIGN-PLAN_DEV_SCM_BUILD_PACKAGE_DEPLOY-TEST_DEPLOY-PROD.png)


---
### 2.2. Pré requisitos

* [Bamboo instalado](https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server/doc/README_InstallBambooLicense_StepByStep.md)
* [Guia de Instalação Bamboo Server para Windows](README-GuiaInstalacao-Bambo-Windows.md)
* [Cobol Free for Linux Instalado](https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server#321-compilador-cobol-free-linux)

---
### 2.3. Leitura pré-execução

* não há

---
### 2.4. Guia de Configuração

* __em construção__

---
### 2.5. Guia de Demonstração

* Passo 01: **Identificar requisitos de negócio #01-01-01**: 
  * a
  * b
  * c
* Passo 02: **Especificar requisitos funcionais #01-01-02**: 
* Passo 03: **Especificar requisitos não funcionais #01-01-03**:
* Passo 04: **Especificar casos de testes #01-01-04**: 
* Passo 05: **Elaborar e Revisar planejamento #01-01-05**:

---
## 3. Conclusão
* Observe que neste cenário o Bamboo fez as atividades de "SCM - Source Code Management", "BUILD - Compilar", de forma automática


---