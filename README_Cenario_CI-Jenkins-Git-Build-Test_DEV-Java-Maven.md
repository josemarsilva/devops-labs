# README - devops-labs - Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven

## 1. Introdução

### 1.1. Objetivo
O objetivo deste cenário é demonstrar a ferramenta **Jenkins** integrando com o **Github** para buscar o código fonte de um aplicativo construído em linguagem **Java**, em seguida o **Jenkins** faz o **Build** com base no **Maven**, executa os testes unitários **Unit Test** já previstas na programação e gera o binário do aplicativo.

### 1.2. MindMap
![MindMap DevOps CI-Jenkins-Git-Build-Test_DEV-Java-Maven.png](doc/MindMap%20DevOps%20CI-Jenkins-Git-Build-Test_DEV-Java-Maven.png)


### 1.3. Tópicos abordados
Este cenário de laboratório aborda os seguintes tópicos, conceitos, práticas e ferramentas:
* CI - Continuos Integration
* Jenkins
* Job do Jenkins executando `git pull`
* Job do Jenkins fazendo o build da aplicação com o Maven
* Automação do processo de Build e UnitTest
* Cultura do compromisso de ter o código fonte em um repositório (neste caso GitHub)

---
## 2. Cenário

### 2.1. Diagramas 

### a. Use Case Diagram

* Diagrama de Contexto do laboratório

![UseCaseDiagram-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven.png](doc/UseCaseDiagram-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven.png)

* Diagrama de Contexto da aplicação `java-simplecalc-cli`
A aplicação [`java-simplecalc-cli` Calculadora Simples em linha de comando](https://github.com/josemarsilva/java-simplecalc-cli) recebe como parâmetro uma expressão, avalia e apresenta o seu resultado.

![java-simplecalc-cli-UseCaseDiagram-Context.png](https://github.com/josemarsilva/java-simplecalc-cli/blob/master/doc/UseCaseDiagram-Context.png)


### b. Deploy Diagram
![DeployDiagram-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven.png](doc/DeployDiagram-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven.png)



### c. BPMN
![BPMN-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven.png](doc/BPMN-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven.png)


---
### 2.2. Pré requisitos

* [Jenkins instalado](https://github.com/josemarsilva/eval-jenkins)
  * [Jenkins instalado Windows](https://github.com/josemarsilva/eval-jenkins/blob/master/doc/README-GuiaConfiguracao-InstallJenkins.md)
* [Novo Job tipo FreeStyle Execute Shell Compila e Executa um programa Java com codigo fonte baixado do GitHub](https://github.com/josemarsilva/eval-jenkins/blob/master/doc/README-GuiaDemonstracao-JobFreestyleExecShellGitJavacJavaRun.md)
* Jenkins Master ou Slave configurado em máquina com Sistema Operacional Windows


---
### 2.3. Leitura pré-execução

* não há

---
### 2.4. Guia de Configuração


---
### 2.5. Guia de Demonstração


---
## 3. Conclusão


---
## I - Referências

* [Java SimpleCalc Cli - Calculadora Simples em linha de comando](https://github.com/josemarsilva/java-simplecalc-cli)
