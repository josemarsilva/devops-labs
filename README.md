# README - devops-labs

## 1. Introdução

### 1.1. Objetivo
O objetivo deste projeto é compilar, organizar, documentar e compartilhar __cenários e laboratórios__, práticas e experiências de **DevOps**.


### 1.2. O que é DevOps
O DevOps é um conjunto de práticas, ferramentas e técnicas que automatizam os processos entre equipes de desenvolvimento de software e a equipe de operação e infraestrutura de TI para que possam criar, testar, liberar e entregar softwares de maneira mais rápida e confiável. Não há consenso sobre uma metodologia única ou padrão. Cada empresa constrói a sua prática.


### 1.3. Como os cenários estão organizados
A estratégia deste projeto é __agrupar__ os cenários e laboratórios em __tópicos__ por critérios comuns e ordem crescente, conforme o estágio de maturidade e complexidade. Será comum encontrar um cenário que referencie um cenário anteriormente descrito, extendendo-o para uma nova funcionalidade (maior maturidade). 

Os cenários serão organizados em tópicos comuns, com objetivo de dar uniformidade a leitura e referência. E também, a organização por __Mapa Mental (Mind Map)__ trará de forma progressiva a consolidação dos conceitos, práticas e experiências de DevOps. Na parte inicial de cada cenário, terá um __Mapa Mental (Mind Map)__ derivado deste abaixo.

![MindMap DevOps](doc/mind-maps/MindMap%20DevOps.png)
[`MindMap DevOps expanded all levels`](doc/mind-maps/MindMap%20DevOps%20-%20all%20expanded.png)



Embora esta documentação agrupe tópicos comuns, vale lembrar que as melhores experiências e resultados com DevOps se dão com a maturidade crescente em vários tópicos simultaneamente. Este comentário é para desencorajar a certeza de sucesso na implantação de DevOps de forma sequencial, grupo a grupo, tópico a tópico do __MindMap__ apresentado. Penso que a melhor estratégia é diluir as iniciativas pelos tópicos, de forma que um tópico suporte a implantação de outro tópico, em uma abordagem crescente de complexidade e completude, sempre suportada pela __Cultura(Culture)__ e __Ferramenta(Tools/Stack)__ e nunca em hipótese alguma abandonar as necessidades do _seu negócio_ . Não é um caminho de sucesso garantido, muito pelo contrário, revisões podem e devem acontecer. É comum encontrar situações onde será necessário abandonar um processo já implantado e funcionando em pról outro processo com maior nível de automatização. Também é comum encontrar situações onde a cultura da empresa tem resistência por medo humano ao crescente grau de automatização.

Os cenários e laboratórios poderão conter os seguintes diagramas, mas não limitando a somente estes:

* Diagrama UML de __Use Case Diagram__ (Caso de Uso)
* Diagrama UML de __Deploy Diagram__ (Implantação)
* Diagrama UML de __Activity Diagram__ (Atividade)
* Diagrama __BMPN Diagrams__ 

Também podem conter qualquer outro tipo de figuras e vídeos com objetivo de enriquecer a documentação do cenário. As ferramenta(s) utilizada(s) para documentar os diagramas são:

* [DrawIo](https://www.draw.io/)
* [Free Mind](https://freemind.br.softonic.com/)
* [Youtube](https://youtube.com)

A medida que a maturidade das práticas e experiências são ampliadas, faz-se necessário reaproveitar cenários e laboratórios anteriores como __cenários base__ a partir do qual a evolução ocorre. Também poderá fazer-se necessário contar uma história (contextualizar) para dar sentido ao cenário.


---
## 2. Documentação

### 2.1. Cenários e Laboratórios


| Cenário     | Detalhamento                    | Cenários base ou referências    |
| :---------- | :------------------------------ | :------------------------------ |
| lab-01 [`Cenario_CI-Jenkins_DEV-Java`](./md/README_Cenario_SCM-Git_CI-Jenkins_DEV-Java.md) | Executa Job do Jenkins (Pipeline) que baixa projeto do GitHub, compila e executa | |
| lab-02 [`Cenario_CI-Jenkins-Git-Build-Test_DEV-Java-Maven`](./md/README_Cenario_SCM-Git_CI-Jenkins-Maven-Build-Test-Package_DEV-Java.md) | Executa Job do Jenkins (Pipeline) que baixa projeto do GitHub, faz o build do projeto usando o Maven, executa os tests UnitTest e compila e empacota o aplicativo para Deploy. | |
| lab-03 [`Cenario_CI-Bamboo-Git-Build-Test-Package_DEV-Java-SpringBoot-Maven`](./md/README_Cenario_SCM-Git_CI-Bamboo-Maven-Build-Test-Package_DEV-Java-SpringBoot.md) | Executa um Projeto/Plano (Pipeline) do Bambo que baixa projeto do SCM(Source Code Management) GitHub, executa o CI(Continuous Integration) com build do projeto usando Maven, executa UnitTest(Testes Unitários) com JUnit e empacota o aplicativo para Deploy. | |
| lab-04 [`Cenario_SCM-Git_CI-Bamboo-Build-Test-Package_DEV-Java-CLI-Maven`](./md/README_Cenario_SCM-Git_CI-Bamboo-Maven-Build-Test-Package_DEV-Java-Cli.md) | Executa um Projeto/Plano(s)/Tarefas (Pipeline) do Bambo que baixa projeto do SCM(Source Code Management)  GitHub, executa o CI(Continuous Integration) com build do projeto usando Maven, executa UnitTest(Testes Unitários) com JUnit e empacota o aplicativo para Deploy. | |
| lab-05 [`Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol`](./md/README_Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol.md) | Executa um projeto/plano/tarefas no Bamboo __Build Plan__, que baixa o projeto do __SCM (Source Code Management)__ pela ferramenta  __BitBucket__, executa o __CI(Continuous Integration)__ com __Build__ (compilação) e o __Package__ (empacotamento) do binário executável. | |
| lab-06 [`Cenario_SCM-BitBucket_CI-Bamboo-Build-Package-UnitTest-IntegrationTest-QualityGate_DEPLOY-SharedFileServer_DEV-Cobol`](./md/README_Cenario_SCM-BitBucket_CI-Bamboo-Build-Package-UnitTest-IntegrationTest-QualityGate_DEPLOY-SharedFileServer_DEV-Cobol.md)  | Trata-se de uma evolução de cenário que executa um projeto/plano/tarefas de construção e implantação no Bamboo __Build Plan__ e  __Deploy Plan__ , que baixa o projeto do __SCM (Source Code Management)__ pela ferramenta  __BitBucket__, executa o __CI(Continuous Integration)__ com __Build__ (compilação), o __Package__ (empacotamento) do binário executável, execução de testes unitarios __Unit Test__ , testes integrados __Integration Test__ , análise de qualidade de código fonte Cobol __Code Quality Analysis__ , avalia e verifica __Quality Gates__ durante o __CI/CD(Continous Integration/Continous Deployment)__ com __DEPLOY__ em diversos ambientes, seja de testes TU - Teste Unitário, TI - Teste Integrado e PROD - Produção. | lab-04 [`Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol`](./md/README_Cenario_SCM-BitBucket_CI-Bamboo-Build-Package_DEV-Cobol.md) |
| lab-07 [`Cenario_CULTURE_Study_DevOps`](./md/README_Cenario_CULTURE_Study_DevOps.md)  | Material de estudo sobre os assuntos: *DEVOPS*. | |
| lab-08 [`Cenario_CULTURE-DEVOPS-SRE`](./md/README_Cenario_CULTURE-DEVOPS-SRE.md)  | Internet Bookmarks de material de estudo sobre os assuntos: *DEVOPS* e *SRE*. | |


---
## I - Referências

* [Learning Become a Devops Engineer](https://www.linkedin.com/learning/paths/become-a-devops-engineer)
* [Flow Diagram of Tools used in Devops](https://medium.com/devops-process-and-tools/flow-diagram-of-tools-used-in-devops-b8d9f944ef21)
* [DevOps Stack Tools](https://www.agilestacks.com/products/devops-stack)
* [DevOps Tutorial for Beginners - Learn DevOps in 7 Hours](https://www.youtube.com/watch?v=hQcFE0RD0cQ)
