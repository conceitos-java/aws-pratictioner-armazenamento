# 💻 AWS Compute Power: Escalando Suas Aplicações na Nuvem! ⚡


## Introdução ✨

Estudos focados nos **Serviços de Computação** da Amazon Web Services (AWS)! 

## Servidores Virtuais e Endereçamento IP 🖥️

A base da computação na nuvem da AWS reside em suas instâncias de servidor virtual e na flexibilidade de endereçamento.

### Amazon EC2 (Elastic Compute Cloud) 💡

* **O que é?** Um serviço web que disponibiliza **capacidade computacional segura e redimensionável na nuvem**. Pense nele como a "máquina virtual" da AWS.
* **Caso de Uso:** Fornece instâncias de servidores com diversas configurações e opções de processamento, memória e rede. É projetado para facilitar a computação em nuvem na escala da web para os desenvolvedores. Pode ser usado para hospedar páginas web dinâmicas, executar bancos de dados, servidores de aplicação, etc.
    * **Observação:** Embora possa hospedar páginas web, **não é a forma mais barata e ágil para sites estáticos** (para isso, o Amazon S3 é geralmente mais indicado).

### IP Elástico (Elastic IP) 💡

* **O que é?** Um **endereço IP estático e público** projetado para computação em nuvem dinâmica. Ele não é associado a uma instância específica, mas sim à sua conta AWS.
* **Caso de Uso:** Permite que seus serviços sejam **expostos sempre no mesmo endereço IP**, mesmo que o host subjacente (instância EC2) seja substituído ou alterado. É útil para manter um IP ativo como porta de entrada e associar IPs dinâmicos a cada provisionamento de uma nova máquina, garantindo que o endereço de acesso à sua aplicação não mude.


## Balanceamento de Carga e Escalabilidade Automática ⚖️

Garanta que suas aplicações lidem com o tráfego de forma eficiente e escalem de acordo com a demanda.

### ELB (Elastic Load Balancing) 💡

* **O que é?** Um serviço que **distribui automaticamente o tráfego de entrada** de aplicações entre diversos destinos, como instâncias do Amazon EC2, contêineres, endereços IP, funções do Lambda e dispositivos virtuais.
* **Caso de Uso:** Lidar com a **carga variável de tráfego** das aplicações, direcionando as requisições de forma equilibrada para manter a performance e a disponibilidade, seja em uma única zona de disponibilidade ou em diversas zonas.

### EC2 Auto Scaling 💡

* **O que é?** Um serviço que **monitora suas aplicações e ajusta automaticamente a capacidade computacional** (número de instâncias EC2) para manter a performance de forma estável e previsível, com o menor custo possível.
* **Caso de Uso:** Garante que você tenha o **número correto de instâncias EC2 disponíveis** para lidar com a carga da sua aplicação, escalando para mais instâncias em picos de demanda e reduzindo em períodos de baixa utilização, otimizando custos e garantindo a resiliência.


## Opções de Pagamento do EC2: Otimizando Custos 💰

A AWS oferece diferentes modelos de precificação para instâncias EC2, permitindo que você otimize os custos com base na sua carga de trabalho.

### On-Demand (Sob Demanda) 💡

* **O que é?** Permite pagar pela capacidade de computação por **hora ou segundo**, sem compromisso de longo prazo.
* **Caso de Uso:** Ideal para **flexibilidade máxima** para cargas de trabalho irregulares, com picos imprevisíveis, ou que não podem ter interrupções (ex: desenvolvimento e testes, picos de tráfego temporários).

### Reserved Instances (Instâncias Reservadas) 💡

* **O que é?** Você se compromete a usar instâncias EC2 por um período de **1 ou 3 anos** em troca de um **desconto significativo** (até 75% em comparação com On-Demand).
* **Caso de Uso:** Perfeito para cargas de trabalho com **demanda estável e previsível**, que exigem capacidade reservada e uso contínuo (ex: servidores de banco de dados, aplicações essenciais 24/7).

### Spot Instances (Instâncias Spot) 💡

* **O que é?** Permite solicitar capacidade EC2 não utilizada da AWS por um **preço muito baixo**, mas as instâncias **podem ser interrompidas pela AWS** com um aviso de dois minutos se a capacidade for necessária.
* **Caso de Uso:** Para cargas de trabalho **tolerantes a falhas, flexíveis e que podem ser interrompidas** sem grande impacto, como processamento em lote, tarefas de machine learning não críticas, renderização de vídeo ou testes.


## Contribua! 🤝

Este repositório está em constante construção. Se você tem sugestões, correções ou quer adicionar seu próprio aprendizado, sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*. Toda contribuição é bem-vinda!

---
