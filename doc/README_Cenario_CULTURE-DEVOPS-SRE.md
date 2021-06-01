# README_Cenario_CULTURE-DEVOPS-SRE.md

## 1. Introdução

O objetivo deste laboratório é prover um conteúdo crítico de estudo inicial e a organização os links de conteúdos para referências e demais materiais sobre *DEVOPS* e *SRE* . Segue o índice:

  * [Conteúdo](#2-conteúdo)
    * [Fundamentos e princípios de SRE (Engenharia de Confiabilidade de Sites)](#21-fundamentos-e-princípios-de-sre-engenharia-de-confiabilidade-de-sites)
    * [Definições iniciais e princípios básicos](#211-definições-iniciais-e-princípios-básicos)
    * [Princípios básicos](#212-princípios-básicos)
    * [A posição do profissional de SRE em uma Squad](#213-a-posição-do-profissional-de-sre-em-uma-squad)
    * [Padrões a serem seguidos e evitados](#214-padrões-a-serem-seguidos-e-evitados)
    * [Glossário de terminologias](#215-glossário-de-terminologias)
    * [Diferenças entre SRE vs DEVOPS](#216-diferenças-entre-sre-vs-devops)
    * [Ganhos econômicos com SRE](#217-ganhos-econômicos-com-sre)
    * [Os fluxos de trabalho de SRE vs DEVOPS](#218-os-fluxos-de-trabalho-de-sre-vs-devops)
      * [DEVOPS - Fluxo de trabalho](#devops---fluxo-de-trabalho)
      * [SRE - Fluxo de trabalho](#sre---fluxo-de-trabalho)
    * [Pirâmide de práticas de SRE](#219-pirâmide-de-práticas-de-sre)
    * [Mapa de Competências do profissional de SRE](#2110-mapa-de-competências-do-profissional-de-sre)
      * [Qual é a finalidade deste papel ou função?](#qual-é-a-finalidade-deste-papel-ou-função)
      * [Quais são as responsabilidades?](#quais-são-as-responsabilidades)
      * [Quais são as atividades ou tarefas?](#quais-são-as-atividades-ou-tarefas)
      * [Quais são as competências técnicas indispensáveis](#quais-são-as-competências-técnicas-indispensáveis)
      * [Quais são as competências técnicas desejáveis](#quais-são-as-competências-técnicas-desejáveis)
      * [Quais são as competências comportamentais indispensáveis](#quais-são-as-competências-comportamentais-indispensáveis)
      * [Qual o perfil comportamental indicado?](#qual-o-perfil-comportamental-indicado)
      * [Quais são os principais desafios e complexidades](#quais-são-os-principais-desafios-e-complexidades)
  * [Referências](#i---references)


## 2. Conteúdo

### 2.1. Fundamentos e princípios de SRE (Engenharia de Confiabilidade de Sites)

#### 2.1.1. Definições iniciais e princípios básicos

* o termo SRE engenheiros da Google em 2003, compartilhado externamente em 2008
* método de gerenciamento de operações e serviços dentro da plataforma tornando o uso dos recuros eficientes tendo como foco a confiabilidade do sistema
* o SRE é um recurso que usa a abordagem de engenharia de sofware às operações de TI

#### 2.1.2. Princípios básicos

a) atender as SLO's com consequencias contratuais; 
b) trabalhar de forma a tornar o dia de amanhã melhor do que o dia de hoje; 
c) ter a capacidade de regular a carga do trabalho para o cliente

#### 2.1.3. A posição do profissional de SRE em uma _Squad_
a) assumir a postura de um "key position"
b) Princípios de Lean IT: 
  * valor
  * fluxo de valor
  * fluxo contínuo
  * produção puxada
  * melhoria contínua
c) não despresar a metodologia mas não esquecer do cliente
  * DEV -> DEVOPS -> SRE -> OPS

#### 2.1.4. Padrões a serem seguidos e evitados

Os seguintes anti-padrões devem ser evitados:

  * cilos ou nichos com mindset's antigos
  * equipe DEV e OPS separadas
  * equipe DEVOPS que não estão em confluência
  * DEVOPS despreza o OPS
  * criação de nichos dentro de DEV
  * DBA abandonando os DEV
  * DEVOPS abandona o DEV

#### 2.1.5. Glossário de terminologias

* SLO: Service Level Objective - o quão bom o sistema deve estar
* SLI: Service Level Identificator - mensuarar os serviços por métricas
* SLA: Service Level Agreement - acordo entre provedor e cliente
* ERROR BUDGET: Limite de falhas sistêmicas sem penalização
* BLAMELESS: Foco em soluções sistêmicas e não em pessoas
* TOIL: Tarefas manuais repetitivas que podem ser automatizadas
* POST MORTEM: Relatórios pós incidentes com dados de RCA (root cause analysis)

#### 2.1.6. Diferenças entre SRE vs DEVOPS

```txt
                                     ---+    +---
  * Objetivo primário: confiabilidade   |    |  * Objetivo primário: velocidade do release
    - Operações                         |    |    - Delivery
    - Resposta a incidentes             |    |    - Automação de release
    - Post Mortem                       |    |    - Builds e ambiente
    - Monitoramento, eventos alertas    | vs |    - Gestão de configuração
    - Planejamento e capacidade         |    |    - Infraestrutura como código
                                     ---+    +---
```

#### 2.1.7. Ganhos econômicos com SRE

* as empresas perceberam que os gastos pós implatanção dos sistemas são muito maiores que os gastos de desenvolvimento
* é preciso reservar 50% para melhorias sistemas e outros 50% para verificação e redução de TOIL
* o profissional ganha protagonismo e não fica esperando um incidente cair no colo para começar a trabalhar

#### 2.1.8. Os fluxos de trabalho de SRE vs DEVOPS

* os fluxos de trabalhos são diferentes porém estão unidos
* o que se diz é: "SRE implementa o DEVOPS"

##### DEVOPS - Fluxo de trabalho

* Code
* Build
* Test
* Release
* Deploy
* Monitor
* Feedback

##### SRE - Fluxo de trabalho

* Foundation & Comunication
* Monitoring & Incident Response
* Observability & Post Mortem
* Test & Release
* Caos Engineering
* Capacity Planning
* User Experience

#### 2.1.9. Pirâmide de práticas de SRE

```txt
          +-----------------+
          | User Experience |
         +-------------------+
         | Capacity Planning |
        +---------------------+
        |   Caos Engineering  |
       +-----------------------+
       |     Test & Release    |
    +----------------------------+
    |Observability & Post Mortem |
  +--------------------------------+
  | Monitoring & Incident Response |
+------------------------------------+
|      Foundation & Comunication     |
+------------------------------------+
```

* Foundation & Comunicação
  * Identificar e Mapear: brainstorm inicial com equipes envolvidas, refinamento de processos e mapeamento dos sistemas
* Monitoring & Incident Response
  * Instrumentar e automatizar: definição de SLI's e SLO's, instrumentação de serviços críticos, criação de alertas e automação no processo de resposta à falhas. 4 Golden Signals: latência, saturação, tráfego ou taxa de erro. VALET: Volumetria, Availability, Latência, Taxa de Error e Tickets)
* Observability & Post Mortens
  * Evolução do monitoramento: concentrar e estruturar logs de eventos e relatórios. Definir, melhorar e integrar dashboards de infra, negócio e APM.
* Test & Releasing
  * Engenharia de lançamento: definir "Error Budget" e melhorar práticas atuais de lançamento de software e possíveis alterações no código fonte para otimizar as automações e diminuir o TOIL.
* Caos Engineering
  * Injeção de falhas: inserção de falhas coordenadas, monitoria, documentação e criação de gates de resiliência sistêmica na solução da aplicação
* Capacity
  * planejamento de capacidade: correlação de dados, geração e validação dos modelos matemáticos, projeção de consumo, análise de limitantes e relatórios de melhorias. SLA garantida.
* User Experience
  * Comprovação final da experiência do usuário em relação aos produtos e serviços da instituição

#### 2.1.10. Mapa de Competências do profissional de SRE

##### Qual é a finalidade deste papel ou função?

  * assegurar a confiabilidade de um software e desenvolver e implementar soluções técnicas para aprimorar a usabilidade de uma plataforma bem como a sua visibilidade

##### Quais são as responsabilidades?

  * atuar de maneira proativa no sistema do produto e também reativa caso necessário
  * automatizar trabalhos repetitivos e desnecessários a fim de melhorar processos e gerar mais simplicidade (diminuir o TOIL)
  * correlacionar diferentes fontes de dados ao ponto de desenvolver maneiras de tornar o ambiente completamente observável e auxiliar na implementação de soluções complexas

##### Quais são as atividades ou tarefas?

  * colabora com arquitetos, engenheiros, PO's, gerentes, equipes de infraestrutura, para planejar e coordonenar mudanças nas aplicações e os processos que as norteiam
  * trabalhar com outras equipes de TI e aplicativos para implementar automação de seus processos e melhorar monitoramento de seus sistemas
  * auxilia em tarefas que envolvam conhecimentos em infraestrutura de forma geral, aplicações e serviços sistêmicos relacionados a business transactions
  * auxiliar a definir junto ao cliente SLO's, SLI's e Error Budget  
  * atuar nas soluções e resoluções de problemas relacionados a serviços de aplicação, infra e integrações
  * evoluir a confiabilidade da arquitetura de uma aplicação, revisando e melhorando seus processos e deixando o ambiente resiliente a falhas
  * melhorar a monitoração atual do ambiente através da técnica de observabilidade
  * executar tarefas orientadas à experiência do cliente e respeito os princípios Lean IT

##### Quais são as competências técnicas indispensáveis

  * princípios de computação em nuvem somado ao conhecimento de algum provedor cloud: AWS, GCP ou Azure
  * uma linguagem de programação voltada à automação: Python, C/C++, Java, NodeJs, R, Javascript
  * conhecimento básico ITSM + ferramentas Service Now, 4BIS, Zendesk, Solarwinds, TopDesk ou Jira
  * sistemas operacionas windows, linux e unix
  * saber fundamental de redes TCP/IP
  * noções em processos de automação de software
  * experiência prática com REST API: GET, POST, PUT, DELETE e PATCH
  * possuir vivência em alguma das ferramentas de APM mais utilizadas no mercado: DataDog, AppDynamics, Dynatrace, Prometheus ou Elastic APM
  * possuir vivência em algumas das ferramentas de IAC (Infra As a Code): Chef, Terraform, Ansible, Puppet ou similares
  * conceitos básicos de conteinerização de aplicações
  * vivência em concentração de logs & eventos sistêmicos: ELK, Elastic Logstash ou Splunk
  * tecnicas de troubleshooting
  * possuir entendimento em arquitetura de microserviços, sistemas distribuídos x monolíticos e métodos auto scaling
  * ter nivel foundation de conhecimentos em bases de dados relacionais & não relacionais: SQL e MongoDB
  * práticas DEVOPS em CI & CD com alguma ferramenta pipeline: Jenkins, Bamboo, Gitlab CI, CodeFresh, UrbanCode ou Github
  * conhecer metodologia Lean IT
  * familiaridade com os conceitos de SLI e SLO e Error Budget
  * compreender as principais diferenças entre ambientes On-Premisse e Clouds
  * vivência em algum versionador de código open source: Git, LibreSource, Bazaar ou Mercurial
  * entender de virtualização clássica vs Cloud Computing
  * possuir noções de metodologia ágil: Kanban, XP ou Scrum

##### Quais são as competências técnicas desejáveis

  * debugging de código fonte
  * orquestração de containers: Rancher, Kubernets ou OpenShift
  * conhecer arquitetura de redes e CDN
  * entendimento de SIEM
  * vivência em database script
  * noções em métodos de testes em QA
  * entendimento sobre atividades de migrations para cloud: CloudEndure ou AWS ADS
  * conhecer múltiplas ferramentas de monitoramento
  * compreender API Gateways
  * conhecimento em duas ou mais linguagens de programação voltada a automação Python, C/C++, Java, NodeJs, R ou Javascript
  * multicloud e Cloud híbrida
  * entendimento em software cloud native
  * noções em algorítimos básicos de IA & machine learning
  * alguma experiência em nível DEV com processos de codagem para apps de automação
  * vivência com times & squads multi-culturais
  * línguas: inglês e espanhol
  * elaborar desenhos de soluções de arquitetura
  * entendimento referente às metodologias DEVOPS: Shift-left & Shift-right

##### Quais são as competências comportamentais indispensáveis

  * confiança
  * comprometimento
  * resiliência
  * comunicação eficaz
  * estar aberto a troca de conhecimentos
  * flexibilidade cognitiva
  * espírito de equipe
  * ser resolutivo
  * inteligência emocional
  * criatividade
  * assertividade

##### Qual o perfil comportamental indicado?

  * espírito empreendedor
  * foco e disciplina
  * possuir técnicas de apresentações orais e visuais
  * saber assumir e controlar riscos calculados
  * ter responsabilidade nas tomadas de decisões
  * ser autodidata

##### Quais são os principais desafios e complexidades

  * implementar soluções técnicas de alta compexidade
  * quebrar silos em equipes devido a mindset antigos
  * auto gerenciamento pessoal em reservar tempo para novos aprendizados e desenvolvimento técnico
  * tomada de decisões de grande impacto
  * não serem vistos como "apagadores de incêndio"
  * manter-se em constante atualização com o mercado de trabalho e suas transformações
  * esforço e flexibilidade em possuir um bom relacionamento com todos os times tanto internos quanto externos


#### 1.11. Mapa de Ferramentas

* Application Lifecycle Management
* Communication & ChatOps
* Knowledge Management & Sharing
* SCM/VCS (Source Code & Version)
* CI - Continous Integration
	- Jenkins, Azure DEVOPS, Gitlab-CI, Github Actions
* Build
* Database management
* Testing
	- Cucumber, Selenium, JMeter
* Deployment
	- Terraform, Cloudformation, Rundeck, Ansible, Puppet, Chef
* Artfact Management
* Cloud / IaaS / PaaS
	- AWS, GCP e Azure
* Orchestration & Scheduling
* BI / Monitoring / Logging
	- Prometheus, Grafana, Stack ELK, Splunk, Graylog, Dynatrace, AppDynamics, DataDog
* Programming Languages
	- Python, Golang, NodeJS

# I - References

* [Jornada SRE - dia 1](https://www.youtube.com/watch?v=_OOtEtHEuVc)
* [Jornada SRE - dia 2](https://www.youtube.com/watch?v=3QPWBylRNcw)
* https://devopsinstitute.com/
* https://sre.google/books/
  * https://static.googleusercontent.com/media/sre.google/pt-BR//static/pdf/building_secure_and_reliable_systems.pdf
  * https://sre.google/workbook/table-of-contents/
* https://github.com/LuckyDudeThakur/EBooks/blob/master/Accelerate%20-%20Building%20and%20Scaling%20High%20Performing%20Technology%20Organisations%20-%20Nicole%20Fergrson.pdf
