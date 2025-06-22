# ☁️ AWS Storage Explorer: Armazenamento na Nuvem! 🚀

## Introdução ✨

Bem-vindo(a) ao meu repositório de estudos focado inteiramente em **Serviços de Armazenamento da Amazon Web Services (AWS)**! 👋 Aqui, você encontrará uma coleção organizada das minhas anotações sobre as diversas soluções de armazenamento que a AWS oferece.

Meu objetivo é duplo: **consolidar meu próprio conhecimento** sobre tópicos cruciais de armazenamento para a **certificação AWS Certified Cloud Practitioner** (e além!), e ao mesmo tempo, oferecer um **recurso para a comunidade**. Acredito que compartilhar o aprendizado ajuda a desmistificar a nuvem, especialmente em um tema tão fundamental quanto o armazenamento de dados.

Espero que te ajude de alguma forma!

## Fundamentos de Gerenciamento na AWS 🛠️

Entender a distinção entre serviços gerenciados e não gerenciados é crucial ao trabalhar com a AWS. Essa compreensão afeta diretamente a **responsabilidade operacional** e a **otimização de recursos**.

### O que significa ser "Gerenciado pela AWS"? 🤔

Quando um serviço é **"totalmente gerenciado pela AWS"**, a Amazon Web Services assume a maior parte das **tarefas operacionais complexas e demoradas**. Isso permite que você e sua equipe se concentrem no que realmente importa: **desenvolver suas aplicações e inovar**, em vez de gerenciar a infraestrutura subjacente.

Pense nisso como a diferença entre ser proprietário de um veículo (não gerenciado, você cuida de tudo) e usar um serviço de transporte por aplicativo (gerenciado, a empresa cuida da manutenção, seguro, etc.).

A AWS cuida de:

* **Provisionamento e Instalação:** Configuração e instalação do software.
* **Aplicação de Patches e Atualizações:** Manutenção do software com as últimas correções de segurança e recursos.
* **Backups:** Gerenciamento dos backups dos seus dados para recuperação em caso de falha.
* **Escalabilidade:** Ajuste automático ou facilitado dos recursos (CPU, memória, armazenamento) conforme a demanda.
* **Monitoramento:** Acompanhamento da saúde e performance do serviço, com alertas para possíveis problemas.
* **Tolerância a Falhas:** Construção do serviço com redundância para garantir alta disponibilidade (ex: Multi-AZ para RDS).

### Quando um Serviço NÃO é Gerenciado pela AWS? 🧑‍💻

Quando um serviço não é gerenciado pela AWS (ou é **gerenciado pelo cliente**), a **responsabilidade por essas tarefas operacionais recai sobre você ou sua equipe**. Um exemplo comum é a instalação de um banco de dados diretamente em uma instância do Amazon EC2.

Nesse cenário, sua equipe seria responsável por:

* Instalar o sistema operacional e o software do banco de dados.
* Configurar o banco de dados.
* Aplicar patches e atualizações de segurança.
* Gerenciar backups e recuperação de desastres.
* Monitorar a performance e a utilização dos recursos.
* Escalar o ambiente manualmente quando necessário.

A principal vantagem de um serviço não gerenciado é ter um **maior controle** sobre a administração do banco de dados e do ambiente. No entanto, isso vem com o **custo de uma maior carga de trabalho e responsabilidade operacional**.


## Serviços de Armazenamento e Banco de Dados em Foco 💾📊

Principais serviços de armazenamento e banco de dados que estou estudando na AWS.

### Amazon Aurora 💡

* **O que é?** Um banco de dados relacional **totalmente gerenciado** pela AWS.
* **Principal Característica:** Pode ser até **5x mais rápido** que o MySQL padrão, combinando a velocidade e disponibilidade dos bancos de dados comerciais com a simplicidade e custo-benefício dos bancos de dados de código aberto.
* **Caso de Uso:** Ideal para aplicações que exigem **alta performance e escalabilidade** em um ambiente relacional, como sistemas de e-commerce, jogos online e aplicações SaaS.

### Amazon DynamoDB 💡

* **O que é?** Um banco de dados NoSQL **totalmente gerenciado** pela AWS.
* **Característica Principal:** Baseado em **chave-valor**, o que o torna excelente para dados não estruturados, com performance em milissegundos para qualquer escala.
* **Caso de Uso:** Perfeito para aplicações que precisam persistir **dados não estruturados de clientes**, como perfis de usuário, carrinhos de compras, dados de sessão, ou para aplicações de jogos e IoT.

### Amazon Neptune 💡

* **O que é?** Um banco de dados NoSQL **totalmente gerenciado** pela AWS, baseado em **grafos**.
* **Característica Principal:** Permite modelar e consultar **relações complexas** entre seus dados. Pode ser utilizado em muitos contextos que representam as conexões do nosso cotidiano.
* **Caso de Uso:** Ideal para cenários que exigem a representação e consulta de relacionamentos complexos, como **redes sociais, sistemas de recomendação, detecção de fraudes** e cadeias logísticas ou empresariais.

### Amazon RDS com MariaDB 💡

* **O que é?** O MariaDB é um banco de dados relacional que pode ser **totalmente gerenciado pela AWS quando utilizado no RDS (Relational Database Service)**.
* **Característica Importante:** Quando instalado diretamente em uma instância EC2, **não é gerenciado pela AWS**. Importante notar que não possui o mesmo ganho de performance (5x mais rápido) que o Amazon Aurora em relação ao MySQL.
* **Caso de Uso:** Para quem busca um banco de dados relacional familiar (compatível com MySQL) com os **benefícios de um serviço gerenciado pela AWS**, diminuindo a necessidade de mão de obra para instalação e manutenção de infraestrutura.

### Amazon S3 (Simple Storage Service) 💡

* **O que é?** Um serviço de **armazenamento de objetos** altamente escalável, durável e disponível na nuvem.
* **Característica Principal:** Armazena dados como **objetos dentro de "buckets" (baldes)**. É ideal para armazenar qualquer tipo de arquivo (imagens, vídeos, documentos, backups, etc.) de forma segura e com alta disponibilidade.
* **Caso de Uso:** Servir **conteúdo estático para sites**, armazenar backups, hospedar data lakes para análise de dados, ou como destino para logs de aplicações. É a base para muitas outras soluções na AWS.


## Otimizando Custos com S3 💰

### Classes de Armazenamento do Amazon S3 📂

Para otimizar custos com o S3, é fundamental entender suas diferentes classes de armazenamento, projetadas para diversos padrões de acesso:

* **Standard:** A opção de armazenamento default do S3. Projetada para dados **acessados frequentemente** que exigem alta disponibilidade e baixa latência.
* **Glacier e Glacier Deep Archive:** Classes de armazenamento mais baratas que o Standard.
    * **Característica:** Quanto menos frequentemente os objetos são acessados, mais baratas se tornam as demais classes (como S3 Standard-Infrequent Access, S3 One Zone-Infrequent Access, Glacier e Glacier Deep Archive).
    * **Caso de Uso:** São ideais para **arquivamento de longo prazo**, onde o tempo de recuperação dos dados pode ser maior. O **Glacier Deep Archive** é a classe mais econômica, perfeita para dados que são raramente (ou nunca) acessados.
* **Intelligent-Tiering:** Uma classe inteligente que **move automaticamente os objetos** entre as classes de armazenamento com base nos padrões de acesso, otimizando os custos **sem intervenção manual**.

### S3 Lifecycle 🔄

* **O que é?** Uma funcionalidade poderosa do Amazon S3 que permite **gerenciar o ciclo de vida dos seus objetos** de forma automatizada.
* **Como funciona?** Você pode definir **regras** para que os objetos sejam movidos automaticamente entre diferentes classes de armazenamento (por exemplo, de Standard para Glacier após 30 dias) ou **excluídos** após um determinado período.
* **Caso de Uso:** Para otimizar o custo com o S3, você pode configurar o S3 Lifecycle para que objetos (como logs antigos) **expirem e sejam automaticamente excluídos** após um determinado número de dias (por exemplo, 30 dias), reduzindo o armazenamento desnecessário e os custos associados.


## Contribua! 🤝

Este repositório está em constante construção. Se você tem sugestões, correções ou quer adicionar seu próprio aprendizado, sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*. Toda contribuição é bem-vinda!

