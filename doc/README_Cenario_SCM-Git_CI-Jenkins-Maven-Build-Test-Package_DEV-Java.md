# README - devops-labs - Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven

## 1. Introdução

### 1.1. Objetivo
O objetivo deste cenário é demonstrar a ferramenta **Jenkins** integrando com o **Github** para buscar o código fonte de um aplicativo construído em linguagem **Java**, em seguida o **Jenkins** faz o **Build** com base no **Maven**, executa os testes unitários **Unit Test** já previstas na programação e gera o binário do aplicativo.

### 1.2. MindMap
![MindMap DevOps SCM-Git_CI-Jenkins-Maven-Build-Test_DEV-Java.png](mind-maps/MindMap%20DevOps%20SCM-Git_CI-Jenkins-Maven-Build-Test_DEV-Java.png)


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


![UseCaseDiagram-Cenario_SCM-Git_CI-Jenkins-Maven-Build-Test_DEV-Java.png](uml-diagrams/UseCaseDiagram-Cenario_SCM-Git_CI-Jenkins-Maven-Build-Test_DEV-Java.png)

* Diagrama de Contexto da aplicação `java-simplecalc-cli`
Esta aplicação implementa uma [Calculadora Simples em linha de comando](https://github.com/josemarsilva/java-simplecalc-cli) recebe como parâmetro uma expressão, avalia e apresenta o seu resultado.

![java-simplecalc-cli-UseCaseDiagram-Context.png](https://github.com/josemarsilva/java-simplecalc-cli/blob/master/doc/UseCaseDiagram-Context.png)


### b. Deploy Diagram
![DeployDiagram-Cenario_SCM_Git_CI-Jenkins-Maven-Build-Test_DEV-Java.png](uml-diagram/DeployDiagram-Cenario_SCM_Git_CI-Jenkins-Maven-Build-Test_DEV-Java.png)



### c. BPMN
![BPMN-Cenario_SCM-Git_CI-Jenkins-Maven-Build-Test_DEV-Java.png](bpmn-diagrams/BPMN-Cenario_SCM-Git_CI-Jenkins-Maven-Build-Test_DEV-Java.png)


---
### 2.2. Pré requisitos

* [Jenkins instalado](https://github.com/josemarsilva/eval-jenkins)
* [Jenkins instalado GCloud em Docker](https://github.com/josemarsilva/googlecloudplatform#gcloud-engine---jenkins-using-docker)
* [Instalação do Plugin Maven Integration](https://github.com/josemarsilva/eval-jenkins/blob/master/doc/README-GuiaConfiguracao-MavenJenkins.md)


---
### 2.3. Leitura pré-execução

* não há

---
### 2.4. Guia de Configuração

* Passo 1: Crie um novo Job chamado com o nome `CI-Jenkins-Git-Build-Test_DEV-Java-Maven` do tipo ``Construir um projeto Maven`

![jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-01.png](doc/jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-01.png)

* Passo 2: Na configuração do Job informe o endereço do repositório `https://github.com/josemarsilva/java-simplecalc-cli.git` do projeto [`java-simplecalc-cli` Calculadora Simples em linha de comando](https://github.com/josemarsilva/java-simplecalc-cli) :

![jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-02.png](doc/jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-02.png)

* Passo 3: Na configuração do Job, na sessão `Construir` informe os __goals__ (metas e opções) do Maven para o projeto: `clean compile test package`

![jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-03.png](doc/jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-03.png)

* Passo 4: Clique no botão `Salvar` para salvar as configurações do Job criada

![jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-04.png](doc/jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-04.png)


---
### 2.5. Guia de Demonstração

* Passo 1: Clique no item do menu lateral esquerdo ![jenkins-icon-buildnow.png](doc/jenkins-icon-buildnow.png) `Construir agora`

* Passo 2: Clique no link ![jenkins-icon-console.png](doc/jenkins-icon-console.png) `Saída do console` para observar os detalhes da execução do job

![jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-05.png](doc/jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-05.png)
![jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-06.png](doc/jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-06.png)
![jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-07.png](doc/jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-07.png)
![jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-08.png](doc/jenkins-printscreen-Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven_Job-08.png)



---
## 3. Conclusão
* Observe que neste cenário o Jenkins fez as atividades de "Source Code Management", "Build", "Unit Test", de forma automática
* Observe que configuramos o __goals__ `package` no Maven e ele gerou o ".jar" da aplicação, porém ainda não fizemos o "Deploy" desta aplicação 

---
## I - Referências

* [Java SimpleCalc Cli - Calculadora Simples em linha de comando](https://github.com/josemarsilva/java-simplecalc-cli)
* [Configurando Jenkins e Maven](https://www.tutorialspoint.com/jenkins/jenkins_maven_setup.htm)
