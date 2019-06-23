# README - devops-labs

## 1. Introdução

### 1.1. Objetivo
O objetivo deste projeto é compilar, organizar e documentar __cenários__ de laboratórios, práticas e experiências de **DevOps**.


### 1.2. O que é DevOps
O DevOps é um conjunto de práticas que automatizam os processos entre equipes de desenvolvimento de software e de TI para que possam criar, testar e liberar softwares de maneira mais rápida e confiável. Não há consenso sobre uma metodologia única ou padrão. Cada empresa constrói a sua prática.


### 1.3. Como os cenários estão organizados
A estratégia deste projeto é __agrupar os cenários em tópicos__ por critérios comuns e ordem crescente de complexidade. Será comum encontrar um cenário que referencie um cenário anteriormente descrito, extendendo-o para uma nova funcionalidade. 

Os cenários serão organizados em tópicos comuns, com objetivo de dar uniformidade a leitura e referência. E também, a organização por __Mapa Mental (Mind Map)__ trará de forma progressiva a consolidação dos conceitos, práticas e experiências de DevOps. Na parte inicial de cada cenário, terá um __Mapa Mental (Mind Map)__ derivado deste abaixo.

![MindMap DevOps](doc/MindMap%20DevOps.png)

Embora esta documentação agrupe tópicos comuns, vale lembrar que as melhores experiências e resultados com DevOps se dão com a maturidade crescente de todos os tópicos. Este comentário é para desencorajar a certeza de sucesso na implantação de DevOps de forma sequencial, grupo a grupo, tópico a tópico do __MindMap__ apresentado. Penso que a melhor estratégia é diluir as iniciativas pelos tópicos, em uma abordagem crescente de complexidade, sempre suportada pela __Cultura (Culture)__ e __Ferramenta (Tools)__. Não é um caminho de sucesso garantido, muito pelo contrário, revisões podem e devem acontecer. É comum encontrar situações onde será necessário abandonar um processo já implantado e funcionando em pról outro processo com maior nível de automatização.

Os cenários poderão conter diagramas de contexto. Serão usados os diagramas UML de __Use Case Diagram__, __Deploy Diagram__, __Activity Diagram__ ,  __BMPN Diagrams__ e qualquer outro tipo de figuras e vídeos com objetivo de enriquecer a documentação do cenário. As ferramenta(s) utilizada(s) para escrever os diagramas são [DrawIo](https://www.draw.io/) e [Free Mind](https://freemind.br.softonic.com/).

A medida que a maturidade das práticas e experiências são ampliadas, faz-se necessário reaproveitar cenários anteriores como __cenários base__ a partir do qual a evolução ocorre. Também poderá fazer-se necessário contar uma história (contextualizar) para dar sentido ao cenário.


---
## 2. Documentação

### 2.1. Cenários

* [`Cenario_CI-Jenkins_DEV-Java`: Executa Job do Jenkins (Pipeline) que baixa projeto do GitHub, compila e executa](README_Cenario_CI-Jenkins_DEV-Java.md)

* [`Cenario_CI-Jenkins-Git-Buld-Test_DEV-Java-Maven`: Executa Job do Jenkins (Pipeline) que baixa projeto do GitHub, faz o build do projeto usando o Maven, com UnitTest e compila e gera o binário do aplicativo para distribuição](README_Cenario_CI-Jenkins-Git-Buld-Test_DEV-Java-Maven.md)


---
## I - Referências

* [Learning Become a Devops Engineer](https://www.linkedin.com/learning/paths/become-a-devops-engineer)
* [Flow Diagram of Tools used in Devops](https://medium.com/devops-process-and-tools/flow-diagram-of-tools-used-in-devops-b8d9f944ef21)
* [DevOps Stack Tools](https://www.agilestacks.com/products/devops-stack)
