# README - devops-labs - Cenario_SCM-Git-CI-Bamboo-Build-Test-Package_DEV-Java-CLI-Maven

## 1. Introdução

### 1.1. Objetivo
O objetivo deste cenário é demonstrar a ferramenta **Bamboo** integrando com o **Github** para buscar o código fonte de um aplicativo construído em linguagem **Java** e **Apache-CLI**. Em seguida o **Bamboo** faz o **Build** com base no **Maven**, executa os testes unitários **Unit Test** já previstas na programação e gera o pacote de aplicativo.

### 1.2. MindMap
![MindMap DevOps SCM-CI-Bamboo-Git-Build-Test-Package_DEV-Java-Cli-Maven.png](doc/MindMap%20DevOps%20SCM-CI-Bamboo-Git-Build-Test-Package_DEV-Java-Cli-Maven.png)


### 1.3. Tópicos abordados
Este cenário de laboratório aborda os seguintes tópicos, conceitos, práticas e ferramentas:
* SCM - Source Code GitHub.com
* CI - Continuos Integration ( Checkout Source Code, Compile, Build, Package )
* Bamboo - CI Tools
* Bamboo Project, Plan e Build executando `git pull`
* Bamboo Project, Plan e Build executando  fazendo o `Build` da aplicação com o `Maven`
* Automação do processo de `Build`, `UnitTest` e `Package`
* Cultura do compromisso de ter o código fonte em um repositório (GitHub)

---
## 2. Cenário

### 2.1. Diagramas 

### a. Use Case Diagram

* Diagrama de Contexto do laboratório

![UseCaseDiagram-Cenario_CI-Bamboo-Git-Build-Test-Package_DEV-Java-SpringBoot-Maven.png](doc/UseCaseDiagram-Cenario_CI-Bamboo-Git-Build-Test-Package_DEV-Java-SpringBoot-Maven.png)

* Diagrama de Contexto da aplicação `java-simplecalc-spring-boot`
A aplicação [`java-simplecalc-spring-boot` Calculadora Simples de expressão pela web](https://github.com/josemarsilva/java-simplecalc-spring-boot) recebe como parâmetro uma expressão, avalia e apresenta o seu resultado.

![java-simplecalc-spring-boot-UseCaseDiagram-Context.png](https://github.com/josemarsilva/java-simplecalc-spring-boot/blob/master/doc/UseCaseDiagram-Context.png)


### b. Deploy Diagram
![DeployDiagram-Cenario_CI-Bamboo-Git-Build-Test-Package_DEV-Java-SpringBoot-Maven.png](doc/DeployDiagram-Cenario_CI-Bamboo-Git-Build-Test-Package_DEV-Java-SpringBoot-Maven.png)



### c. BPMN
![BPMN-Cenario_SCM-Git_CI-Bamboo-Maven-Build-Test-Package_DEV-Java-Cli.png](doc/BPMN-Cenario_SCM-Git_CI-Bamboo-Maven-Build-Test-Package_DEV-Java-Cli.png)


---
### 2.2. Pré requisitos

* [Bamboo instalado](https://github.com/josemarsilva/eval-virtualbox-vm-ubuntu-server/doc/README_InstallBambooLicense_StepByStep.md)
* [Guia de Instalação Bamboo Server para Windows](README-GuiaInstalacao-Bambo-Windows.md)
* Maven 3.6.x instaldo


---
### 2.3. Leitura pré-execução

* não há

---
### 2.4. Guia de Configuração
O objetivo é você criar um **projeto** (__project__), **plano** (__plan__) e **construção** (__build__) para realizar o download do código do GitHub e fazer o `Build` e o `Package`.

* Passo 1: Efetue o login no Bamboo Server

![bamboo-printscreen-javasimplecalccli-01-login.png](doc/bamboo-printscreen-javasimplecalccli-01-login.png)



---
### 2.5. Guia de Demonstração

* under-construction


---
## 3. Conclusão
* Observe que neste cenário o Bamboo fez as atividades de "Source Code Management", "Build", "Unit Test", de forma automática
* Observe que configuramos o __goals__ `clean compile pacakge` no Maven e ele gerou o ".jar" da aplicação, porém ainda não fizemos o "Deploy" desta aplicação 

---
## I - Referências

* [`java-simplecalc-spring-boot` Calculadora Simples de expressão pela web](https://github.com/josemarsilva/java-simplecalc-spring-boot)
* [Site Atlassian sobre Bamboo](https://br.atlassian.com/software/bamboo)
* [Bitbucket Pipeline Build and Deploy](https://bitbucket.org/product/features/pipelines)
* [Vídeo Youtub - Getting Started with Atlassian Bamboo - Continuous Delivery in Action](https://www.youtube.com/watch?v=rG-XxVYNS4c)
* [Bamboo vs Jenkins: Which CI/CD tool to use?](https://blog.valiantys.com/en/dev-tools-en/jenkins-vs-bamboo/)
* [Bamboo vs Jenkins](https://www.automation-consultants.com/bamboo-vs-jenkins/)
