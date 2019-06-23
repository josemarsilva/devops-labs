# README - devops-labs - Cenario_CI-Jenkins-Git_DEV-Java

## 1. Introdução

### 1.1. Objetivo
O objetivo deste cenário é demonstrar a ferramenta **Jenkins** integrando com o **Github** para buscar o código fonte de um aplicativo construído em linguagem **Java**, em seguida compila o aplicativo gerando um código executável e finalmente aplicativo.

### 1.2. MindMap
![MindMap DevOps CI-Jenkins-Git_DEV-Java.png](doc/MindMap%20DevOps%20CI-Jenkins-Git_DEV-Java.png)


### 1.3. Tópicos abordados
No cenário de laboratório, é possível abordar tópicos dos seguintes conceitos, práticas e ferramentas:
* CI - Continuos Integration
* Jenkins
* Job do Jenkins executando `git pull`
* Job do Jenkins compilando um programa Java
* Job do Jenkins executando uma classe Java
* Linguagem de programação **Java**


---
## 2. Cenário

### 2.1. Diagramas 

### a. Use Case Diagram
* Diagrama de Contexto: Jenkins pipeline orquestrando compilação e execução do programa Java `Hello`
![UseCaseDiagram-Cenario_CI-Jenkins-Git_DEV-Java.png](doc/UseCaseDiagram-Cenario_CI-Jenkins-Git_DEV-Java.png)


### b. Deploy Diagram
![DeployDiagram-Cenario_CI-Jenkins-Git_DEV-Java.png](doc/DeployDiagram-Cenario_CI-Jenkins-Git_DEV-Java.png)

### c. BPMN
"[BPMN-Cenario_CI-Jenkins-Git_DEV-Java.png](BPMN-Cenario_CI-Jenkins-Git_DEV-Java.png)


---
### 2.2. Pré requisitos

* [Jenkins instalado](https://github.com/josemarsilva/eval-jenkins)
  * [Jenkins instalado Windows](https://github.com/josemarsilva/eval-jenkins/blob/master/doc/README-GuiaConfiguracao-InstallJenkins.md)
* [Novo Job tipo FreeStyle Execute Shell Compila e Executa um programa Java com codigo fonte baixado do GitHub](https://github.com/josemarsilva/eval-jenkins/blob/master/doc/README-GuiaDemonstracao-JobFreestyleExecShellGitJavacJavaRun.md)
* Jenkins Master ou Slave configurado em máquina com Sistema Operacional Windows


---
## 3. Conclusão

* Conforme podemos observar, neste cenário o Jenkins fez as atividades de "Source Code Management", "Build", "Deploy" e "Execute" tudo junto e muito monolítico. Não é a melhor forma de construir


---
## I - Referências

* [Jenkins instalado](https://github.com/josemarsilva/eval-jenkins)
