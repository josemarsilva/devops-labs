# README - devops-labs - Cenario_SCM-BitBucket_CI-Bamboo-Build-Package-UnitTest-IntegrationTest-QualityGate_DEPLOY-SharedFileServer_DEV-Cobol

## 1. Introdução

### 1.1. Objetivo
O objetivo deste cenário é demonstrar a ferramenta de **CI**: **Bamboo** integrando com a ferramenta de **SCM**: **BitBucket** para buscar o código fonte de um aplicativo construído em linguagem de programação **Cobol** . Em seguida o **CI** / **Bamboo** faz o **CI** / **Build** com base no **Compilador Cobol Free**, gera o **CI** / **Package** do programa objeto executável e executa um pacote de scripts de testes.

Em seguida são feitos **Testes** do tipo **Unit Test**, **Integration Test** e **Code Quality Analysis** e verificado os **Quality Gates** antes de realizar o **DEPLOY**. O **DEPLOY** promove o pacote entre os ambientes de `TU` - Teste Unitário, `TI` - Teste Integrado até o último ambiente `PROD` - Produção.

* `ATENÇÃO`: Este cenário é uma evolução do cenário [Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol](README_Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol.md).

### 1.2. MindMap
![MindMap DevOps SCM-BitBucket_CI-Bamboo-Build-Package-UnitTest-IntegrationTest-QualityGate_DEPLOY-SharedFileServer_DEV-Cobol.png](mind-maps/MindMap%20DevOps%20SCM-BitBucket_CI-Bamboo-Build-Package-UnitTest-IntegrationTest-QualityGate_DEPLOY-SharedFileServer_DEV-Cobol.png)


### 1.3. Tópicos abordados
Este cenário de laboratório aborda os seguintes tópicos, conceitos, práticas e ferramentas:

* Requirement Management - Requisito de negócio foi identificado e especificado
* SCM - Source Code - BitBucket.org
* Programming Language - Cobol
* CI - Continuos Integration ( Checkout Source Code, Compile, Build, Package )
* TEST - Unit Test, Integration Test, Code Quality Analysis e Quality Gates
* DEPLOY - Environments of Unit Test, Integration Test and Production
* Stack Tools Used: Cobol Free/Linux, BitBucket.com, Bamboo

---
## 2. Cenário

### 2.1. Diagramas 

### a. Use Case Diagram

* Diagrama Caso de Uso - `cobol-hello-world`

![UseCaseDiagram-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol.png](uml-diagrams/UseCaseDiagram-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol.png)


### b. Deploy Diagram

* Diagrama de Implantação - `cobol-hello-world`

![DeployDiagram-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol.png](uml-diagrams/DeployDiagram-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol.png)



### c. BPMN

* Diagrama BPMN - Contexto DevOps Labs Pipeline - `01`

![BPMN-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package-UnitTest-IntegrationTest-QualityGate_DEPLOY-SharedFileServer_DEV-Cobol_01.png](bpmn-diagrams/BPMN-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package-UnitTest-IntegrationTest-QualityGate_DEPLOY-SharedFileServer_DEV-Cobol_01.png)

* Diagrama BPMN - PLAN - Design e Planejamento - `01-01`

![BPMN-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol_01-01.png](bpmn-diagrams/BPMN-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol_01-01.png)

* Diagrama BPMN - DEV - Desenvolvimento - `01-02`

![BPMN-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol_01-02.png](bpmn-diagrams/BPMN-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol_01-02.png)

* Diagrama BPMN - SCM - Desenvolvimento - `01-03`

![BPMN-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol_01-03.png](bpmn-diagrams/BPMN-Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol_01-03.png)

* Diagrama BPMN - BUILD - Compilação e Construção - `01-04`

* Diagrama BPMN - PACKAGE REPOSITORY - Empacotar o entregável - `01-05`

* Diagrama BPMN - DEPLOY - Distribuir ambiente(s) de Teste Unitário - `01-06`

* Diagrama BPMN - DEPLOY - Distribuir ambiente(s) de Teste Integrado - `01-07`

* Diagrama BPMN - DEPLOY - Distribuir ambiente(s) de Teste Produção - `01-08`

---
### 2.2. Pré requisitos

* [Container Docker com Bamboo instalado](https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server/#414-docker---bamboo-server)
* [Ativação da licensa de uso do Bamboo](https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server/blob/master/doc/README_InstallBambooLicense_StepByStep.md)
* [Guia de Instalação Bamboo Server para Windows](README-GuiaInstalacao-Bambo-Windows.md)
* [Cobol Free for Linux Instalado](https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server#321-compilador-cobol-free-linux)
* [Devops Labs Script Project](https://github.com/josemarsilva/devops-labs-scripts)

---
### 2.3. Leitura pré-execução

* não há

---
### 2.4. Guia de Configuração

* __em construção__

---
### 2.5. Guia de Demonstração

* Passo 01: `BPMN - Identificar requisitos de negócio #01-01-01`: 
  * O time de analistas de negócio identificou a demanda: __precisamos dizer "Olá" em inglês para expandir a atuação a clientes internacionais__
* Passo 02: `BPMN - Especificar requisitos funcionais #01-01-02`: 
  * O time de analistas de sistemas especificou os requisitos do sistemas que deve ser construído:
    * Construir um programa que ao ser executado informe a mensagem "Olá mundo" em inglês, istoé "hello world"
    * É importante o programa coletar métricas de quandos clientes novos foram conquistados
* Passo 03: `BPMN - Especificar requisitos não funcionais #01-01-03`:
    * O sistema deve ser construído na linguagem de programação **Cobol**
    * O sistema deve ser construído para ser entregue pela esteira DevOps do laboratório
    * A esteira DevOps deve implementar:
	  * **SCM**: Controle de versões pelo **BitBucket*
	  * **CI**: Integração **contínua** na ferramenta **Bamboo** entre versão de fontes, **compilação** e **empacotamento**
* Passo 04: `BPMN - Especificar casos de testes #01-01-04`: 
  * O time de analistas de testes especificou os Casos de Testes que devem ser construído:
    * Construir o caso de teste unitário: quando o programa for iniciado, verificar se a mensagem "Hello" foi apresentada
    * Construir o caso de teste integrado: que valide a quantidade de Hello's contabilizados com um log de execução
* Passo 05: `BPMN - Elaborar e Revisar planejamento #01-01-05`:
  * Em conjunto, os times de analistas de negócios, analistas de sistemas e analistas de testes elaboraram e revisaram o planejamento do desenvolvimento do sistema
    * Cronograma construído: 2h para desenvolvimento

---
## 3. Conclusão
* Observe que neste cenário o Bamboo fez as atividades de "SCM - Source Code Management", "BUILD - Compilar", de forma automática


---