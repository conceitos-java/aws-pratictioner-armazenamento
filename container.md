# 📦 AWS Container Services: Orquestrando Aplicações na Nuvem! 🚀


## Introdução ✨

Estudos dedicados aos **Serviços de Contêineres** da Amazon Web Services (AWS)! 

## Orquestração de Contêineres 🌐

A orquestração é o coração das arquiteturas de contêineres, gerenciando o ciclo de vida, o escalonamento e a rede de suas aplicações.

### Amazon ECS (Elastic Container Service) 💡

* **O que é?** Um serviço **totalmente gerenciado de orquestração de contêineres** que ajuda a implantar, gerenciar e escalar facilmente aplicações conteinerizadas. É a própria solução da AWS para orquestração.
* **Caso de Uso:** Ideal se você está começando com contêineres na AWS e deseja uma **solução nativa e integrada** que simplifique a operação. É excelente para times que buscam uma arquitetura de microsserviços com contêineres sem a complexidade de gerenciar um orquestrador.

### Amazon EKS (Elastic Kubernetes Service) 💡

* **O que é?** Um serviço **totalmente gerenciado que executa o plano de controle e orquestração de contêineres com Kubernetes** em várias zonas de disponibilidade. Ele abstrai a complexidade da instalação e manutenção do Kubernetes.
* **Caso de Uso:** Para quem **já utiliza ou planeja utilizar Kubernetes** e deseja a facilidade de um serviço gerenciado pela AWS. O EKS detecta e substitui nós com problemas, e oferece atualizações do plano de controle sem tempo de inatividade, permitindo que você se concentre nas suas aplicações.



## Registro de Imagens de Contêineres 🗄️

Onde suas imagens de contêineres são armazenadas, gerenciadas e versionadas.

### Amazon ECR (Elastic Container Registry) 💡

* **O que é?** Um **registro de contêiner totalmente gerenciado** que facilita o armazenamento, o gerenciamento, o compartilhamento e a implantação de imagens e artefatos de contêiner em qualquer lugar.
* **Caso de Uso:** Atua como um **repositório seguro e escalável para suas imagens Docker** e outros artefatos de contêiner. É totalmente integrado com o ECS, EKS e AWS Lambda, simplificando o fluxo de trabalho de desenvolvimento e implantação.



## Contêineres Serverless: Sem Se Preocupar com Servidores! ✨

Para uma experiência de contêineres com o mínimo de gerenciamento de infraestrutura.

### AWS Fargate 💡

* **O que é?** Uma **tecnologia de computação serverless** para o Amazon ECS e Amazon EKS que permite que você execute contêineres **sem precisar provisionar ou gerenciar servidores** (instâncias EC2). Você paga apenas pelos recursos de computação que seus contêineres consomem.
* **Caso de Uso:** Ideal para uma abordagem **serverless com contêineres** que busca máxima **velocidade nas entregas**, uma vez que você não precisa se preocupar com questões de infraestrutura de servidores, patching, escalonamento de hosts, etc. Perfeito para microsserviços e aplicações que demandam alta agilidade e baixo overhead operacional.



## Contribua! 🤝

Este repositório está em constante construção. Se você tem sugestões, correções ou quer adicionar seu próprio aprendizado, sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*. Toda contribuição é bem-vinda!

