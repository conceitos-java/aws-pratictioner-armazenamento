# ⚡ AWS Messaging & Orchestration: Fluxos de Dados e Automação na Nuvem! 🚀


## Introdução ✨

Estudos focados na categoria **Mensageria, Eventos e Orquestração** da Amazon Web Services (AWS)! 

### AWS Lambda 💡

* **O que é?** Um serviço de computação serverless (sem servidor) que executa seu código em resposta a eventos.
* **Característica Principal:** Você não precisa gerenciar servidores. A AWS cuida de todo o provisionamento e gerenciamento da infraestrutura para executar suas funções.
* **Caso de Uso:** Pode ser acionado por diversos serviços, como uma alteração em um bucket S3 ou uma chamada de API via API Gateway, para processar dados sem a necessidade de uma infraestrutura dedicada.

## Serviços de Mensageria e Eventos 📬

Esses serviços são a espinha dorsal para construir **sistemas desacoplados e orientados a eventos**, permitindo que diferentes componentes se comuniquem de forma assíncrona e escalável.

### Amazon SQS (Simple Queue Service) 💡

* **O que é?** Um serviço de **filas de mensagens** totalmente gerenciado que permite desacoplar e escalar microsserviços, sistemas distribuídos e aplicações serverless.
* **Caso de Uso:** Ideal para **enfileirar mensagens**, desacoplar os serviços dos sistemas, garantindo que as mensagens sejam entregues de forma confiável, mesmo que o serviço consumidor esteja temporariamente indisponível. Pense em uma fila de tarefas a serem processadas.

### Amazon SNS (Simple Notification Service) 💡

* **O que é?** Um serviço de mensagens de **publicação/assinatura (pub/sub)** totalmente gerenciado, que permite enviar mensagens para múltiplos inscritos (endpoints) de forma assíncrona.
* **Caso de Uso:** Enviar **notificações para usuários** via SMS, e-mail, push notifications, ou enviar mensagens para **outros serviços da AWS** (como o AWS Lambda) em resposta a eventos. Perfeito para comunicar um evento para diversos interessados ao mesmo tempo.

### Amazon EventBridge 💡

* **O que é?** Um **barramento de eventos serverless** que torna mais fácil a criação de aplicações orientadas por eventos em escala. Permite rotear eventos de suas aplicações, aplicações SaaS integradas e serviços da AWS para alvos.
* **Caso de Uso:** Facilitar a criação de **arquiteturas orientadas a eventos**, onde diferentes partes de um sistema se comunicam por meio de eventos. Ele atua como um "corretor" central de eventos, permitindo reações automatizadas a mudanças de estado em qualquer parte do seu ecossistema.

## Orquestração de Workflows 🌐

Para processos que envolvem múltiplos passos e dependências, a orquestração se torna fundamental.

### AWS Step Functions 💡

* **O que é?** Um serviço serverless que facilita a **coordenação de componentes de aplicações distribuídas** usando fluxos de trabalho visuais.
* **Caso de Uso:** Utilizado para **orquestrar partes de uma arquitetura de sistemas baseada em computação sem servidor** (que utiliza S3, API Gateway, Lambda, SQS, SNS), definindo e controlando os possíveis workflows (fluxos de trabalho) de forma sequencial ou paralela. É o serviço mais indicado para automatizar processos que executam diversas tarefas de forma sequencial em seu sistema, com tratamento de erros e retentativas integrados.


## Processamento de Streams de Dados 📈

Quando você precisa lidar com grandes volumes de dados que chegam continuamente, os serviços de stream são a solução.

### AWS Kinesis 💡

* **O que é?** Uma família de serviços para trabalhar com **streams de dados em tempo real**, permitindo coletar, processar e analisar grandes volumes de dados que chegam continuamente.
* **Caso de Uso:** Coletar uma **grande quantidade de dados de aplicações e transferi-los para outros serviços através de streaming** (transmissão contínua), como para análise em tempo real, monitoramento de logs em tempo real, ou armazenamento para processamento posterior (data lakes).


## Contribua! 🤝

Este repositório está em constante construção. Se você tem sugestões, correções ou quer adicionar seu próprio aprendizado, sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*. Toda contribuição é bem-vinda!

