# Proposta de Tema de PI3
**Título:** Futebol de robôs: modelagem e implementação eletrônica

**Aluno(s):** Francisco Eduardo Gonçalves

**Orientador:** Prof. Ênio dos Santos Silva

# Objetivo geral
> O objetivo geral expressa a ação que irá definir o projeto em um sentido amplo.

Este projeto visa conceber, projetar e implementar uma equipe completa de seis robôs autônomos para competição de futebol de robôs. O controle da equipe será centralizado em um software que utilizará técnicas de visão computacional, por meio de uma câmera externa, para monitorar o campo de jogo e coordenar as ações dos robôs em tempo real. A comunicação entre o computador central e cada robô será estabelecida via rádio frequência, garantindo uma resposta rápida e sincronizada durante a partida.

# Objetivos específicos
> Os objetivos específicos são as diferentes ações a serem tomadas durante o desenvolvimento visando concretizar o objetivo geral.

Para alcançar o objetivo principal, os seguintes marcos de desenvolvimento foram definidos:

* **Pesquisa e Aquisição de Componentes:** Realizar uma pesquisa de mercado detalhada para selecionar e adquirir todos os componentes eletrônicos e materiais estruturais necessários para a construção dos seis robôs.
* **Projeto e Construção Mecânica:** Desenvolver o design da estrutura física dos robôs, incluindo chassi e sistemas de acoplamento, e proceder com a montagem mecânica de cada unidade.
* **Desenvolvimento da Locomoção:** Projetar e implementar o sistema de motorização e controle de movimento, garantindo agilidade e precisão na locomoção dos robôs.
* **Projeto e Fabricação da PCB:** Desenhar o layout da Placa de Circuito Impresso (PCB) para integrar de forma otimizada todos os componentes eletrônicos, e em seguida, fabricar as placas.
* **Implementação da Comunicação:** Configurar e validar o sistema de comunicação sem fio via rádio frequência, assegurando uma troca de dados estável e confiável entre o software de controle e os robôs.
* **Integração da Visão Computacional:** Integrar e adaptar o sistema de visão computacional existente para identificar e rastrear os robôs da equipe, os adversários e a bola no campo de jogo.
* **Desenvolvimento de Estratégia de Jogo:** Criar e implementar algoritmos de inteligência artificial que definam as estratégias de jogo, incluindo posicionamento, táticas de ataque, defesa e tomada de decisão em tempo real.

# Metodologia
> Descreve a metodologia de desenvolvimento destacando quais são as etapas.

A execução do projeto seguirá uma abordagem estruturada em fases sequenciais e iterativas, detalhadas abaixo:

1.  **Estudo de Projetos de Referência:** A fase inicial será dedicada a uma imersão teórica, estudando a fundo o projeto de referência "Caboclinhos" da UFS para compreender seus fundamentos de hardware, software e estratégias. Simultaneamente, será conduzida uma pesquisa sobre outras equipes e abordagens no cenário do futebol de robôs para incorporar inovações e melhores práticas ao projeto.

2.  **Desenvolvimento da Parte Mecânica:** Com base no estudo, inicia-se o projeto da estrutura mecânica. A carcaça e a base serão modeladas em software CAD e fabricadas em acrílico, buscando um design que equilibre resistência, baixo peso e agilidade. A seleção de motores e rodas será criteriosa para garantir o torque e a velocidade necessários para um desempenho competitivo.

3.  **Desenvolvimento da Parte Eletrônica:** Esta etapa foca na "inteligência" embarcada. O cérebro de cada robô será o microcontrolador PIC16F873A. O controle dos motores será gerenciado pela ponte H L293D, e a comunicação sem fio será realizada pelo módulo NRF24L01+. A placa de circuito impresso (PCB) será projetada para integrar esses e outros componentes de forma compacta e eficiente, passando por simulações antes da fabricação e montagem.

4.  **Integração Físico-Eletrônica:** Nesta fase, os mundos mecânico e eletrônico se unem. As PCBs montadas e testadas serão cuidadosamente instaladas na estrutura física dos robôs. Serão realizados ajustes finos no posicionamento de sensores e motores. A identidade visual da equipe também será criada, atribuindo cores únicas a cada robô para facilitar a identificação pelo sistema de visão computacional.

5.  **Preparação do Ambiente de Software:** O ambiente de desenvolvimento no computador central será configurado. Isso envolve a instalação de bibliotecas e ferramentas específicas como OpenCV 2.4.11, CMake 3.2.3 e QT Creator 5.5.0. O objetivo é preparar a base de software para se comunicar com o hardware dos robôs.

6.  **Programação da Estratégia do Time:** Com a comunicação estabelecida, esta etapa consiste em programar a inteligência do time. Serão desenvolvidos algoritmos para táticas de jogo, como formações defensivas, jogadas de ataque e comportamento reativo com base na posição da bola e dos oponentes.

7.  **Montagem da Estrutura de Campo:** A preparação do ambiente físico de teste é crucial. Uma estrutura será montada para posicionar a câmera de visão computacional em um ângulo que ofereça uma visão completa e sem obstruções do campo. O transmissor de rádio também será posicionado para otimizar a cobertura do sinal.

8.  **Testes e Aprimoramentos:** A etapa final é um ciclo contínuo de testes e otimização. Os robôs serão colocados em campo para executar as estratégias programadas. O comportamento será analisado para identificar falhas, bugs e oportunidades de melhoria, seja no código, na eletrônica ou na mecânica, visando o máximo desempenho do time.

# Cronograma
> Crie um projeto no GitHub discriminando as ações e o período em que as mesmas serão realizadas. Coloque dentro do parênteses abaixo o link para o projeto criado.

O desenvolvimento do projeto está planejado para ocorrer entre abril e julho de 2025, conforme o cronograma detalhado na tabela abaixo.

| Etapa | Início | Término |
| :--- | :--- | :--- |
| Estudo de projetos de referência | 03/04/2025 | 10/04/2025 |
| Desenvolvimento da parte mecânica dos robôs | 10/04/2025 | 24/04/2025 |
| Desenvolvimento da parte eletrônica dos robôs | 24/04/2025 | 15/05/2025 |
| Integração da estrutura física com o sistema eletrônico | 15/05/2025 | 22/05/2025 |
| Preparação de ambiente de programação | 22/05/2025 | 29/05/2025 |
| Programação de estratégia do time | 29/05/2025 | 19/06/2025 |
| Preparação física do campo e estrutura de todas as peças | 19/06/2025 | 03/07/2025 |
| Testes e aprimoramentos | 03/07/2025 | 16/07/2025 |

***Obs: Não foi possível criar o projeto no Github, pois não tenho acesso a sua conta.***

# Lista de materiais
> Crie uma lista dos materiais que serão necessários para a execução do projeto.

| Item | Descrição | Unidade | Quantidade |
| :--- | :--- | :--- | :--- |
| 01 | Peças de acrílico para o chassi | unidade | 6 |
| 02 | Rodas de alto desempenho | unidade | 24 |
| 03 | Bateria recarregável | unidade | 6 |
| 04 | Cabo flat para conexões internas | metro | 5 |
| 05 | Placas de circuito impresso virgens | unidade | 6 |
| 06 | Microcontrolador PIC16F873a | unidade | 6 |
| 07 | Circuito Integrado MAX232 (Conversor de nível lógico) | unidade | 6 |
| 08 | Circuito Integrado L293D (Ponte H) | unidade | 12 |
| 09 | Regulador de Tensão LM317 | unidade | 6 |
| 10 | Regulador de Tensão LM7805 | unidade | 6 |
| 11 | Módulo de Rádio NRF24L01+ com antena | unidade | 7 |
| 12 | Cristal Oscilador 20 MHz | unidade | 12 |
| 13 | Capacitor cerâmico (diversos valores) | unidade | 50 |
| 14 | Capacitor eletrolítico (diversos valores) | unidade | 30 |
| 15 | Resistores (diversos valores) | unidade | 100 |
| 16 | LEDs de alto brilho | unidade | 30 |
| 17 | Barras de pinos (macho e fêmea) | unidade | 20 |
| 18 | Botões (push-buttons) | unidade | 12 |
| 19 | Kit de Jumpers para prototipagem | kit | 2 |
| 20 | Parafusos de fixação (diversos) | cento | 1 |
| 21 | Porcas de fixação (diversas) | cento | 1 |
| 22 | Arruelas (diversas) | cento | 1 |
| 23 | Conectores de alimentação | unidade | 12 |
| 24 | Placas de fibra de vidro virgem (8cm x 6cm) | unidade | 6 |
| 25 | Conector DB9 fêmea | unidade | 1 |
| 26 | Câmera de vídeo para visão computacional | unidade | 1 |
| 27 | Filamento de impressora 3D para suportes | rolo | 1 |

# Unidades curriculares envolvidas
> Liste as unidades curriculares envolvidas com o tema escolhido.

O conhecimento adquirido em diversas disciplinas do curso será fundamental para o sucesso deste projeto, que possui um caráter multidisciplinar. As principais unidades curriculares envolvidas são:

-   **Programação 1 e 2:** Base para o desenvolvimento do software de controle e da lógica de programação embarcada.
-   **Eletrônica 1 e 2:** Essencial para o projeto dos circuitos, seleção de componentes e montagem da parte eletrônica.
-   **Microcontroladores:** Aplicação direta no controle de baixo nível dos robôs, gerenciando motores e sensores.
-   **Sistemas de Comunicação:** Fundamental para a implementação da comunicação sem fio entre os robôs e o sistema central.
-   **Desenho Técnico:** Utilizado no projeto e modelagem das peças mecânicas e da estrutura dos robôs.
-   **Física 1 (Fundamentos de Mecânica):** Conhecimentos aplicados na análise da dinâmica, estabilidade e movimento dos robôs.
-   **Instrumentação Eletrônica:** Relevante para os processos de teste, medição de sinais e calibração dos sensores e atuadores.