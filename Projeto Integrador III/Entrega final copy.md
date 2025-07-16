
# Título do Trabalho
**Futebol de Robôs: Modelagem e Implementação Eletrônica**

## Introdução

O presente trabalho detalha o processo de desenvolvimento de um protótipo funcional para competições de futebol de robôs. O projeto, inserido na categoria VSS (Very Small Size), tem como objetivo central a criação de um robô controlado remotamente via software, utilizando comunicação por rádio frequência e um sistema de visão computacional para a percepção do ambiente de jogo. Ao longo deste desenvolvimento, foi construído um robô completo e funcional, e o sistema de visão foi implementado de maneira inovadora, utilizando um smartphone com o aplicativo DroidCam para transmitir o vídeo do campo para o computador de controle, demonstrando uma solução de baixo custo e alta flexibilidade para a captura de imagens.

## Revisão da Literatura

Um dos principais trabalhos que serviram como referência e inspiração para este projeto é o **"Caboclinhos"**, desenvolvido pelo Grupo de Pesquisa em Robótica da Universidade Federal de Sergipe (UFS).

O projeto Caboclinhos é uma equipe consolidada na categoria IEEE Very Small Size (VSS) do futebol de robôs, que se destaca pela robustez de seus robôs e pela sofisticação de suas estratégias de software. O objetivo deles é desenvolver uma equipe completa, com múltiplos robôs coordenados por uma inteligência artificial que processa uma visão global do campo para tomar decisões táticas.

**Pontos Positivos do "Caboclinhos":**
* **Sistema Integrado:** Possuem uma solução completa e bem documentada que integra mecânica, eletrônica e software.
* **Estratégia Avançada:** O software de controle implementa algoritmos complexos para posicionamento, defesa e ataque coordenado.
* **Hardware Robusto:** Os robôs são projetados para resistir ao ambiente competitivo e possuem locomoção ágil.

**Diferenças e Pontos Negativos (no contexto deste projeto):**
* **Complexidade:** A implementação completa do sistema Caboclinhos exige um tempo e recursos consideráveis, sendo inviável para um escopo mais limitado.
* **Custo de Visão:** Tradicionalmente, a categoria utiliza câmeras industriais de alta velocidade, que possuem um custo elevado.

O presente trabalho diferencia-se ao focar na construção de um **único protótipo** como prova de conceito, validando os subsistemas de locomoção e comunicação. A principal inovação foi a substituição da câmera industrial por uma solução acessível (DroidCam), contornando o ponto negativo do custo e complexidade do sistema de visão, ainda que com limitações de performance que podem ser exploradas em trabalhos futuros.

## Materiais e Métodos

### Materiais

Para a construção do protótipo funcional, foram utilizados os seguintes componentes:

* **Estrutura:** Peças de acrílico cortadas a laser para o chassi.
* **Locomoção:** 4 rodas de alto desempenho e 4 micromotores DC.
* **Eletrônica:**
    * 1x Placa de Circuito Impresso (PCB) customizada.
    * 1x Microcontrolador PIC16F873a.
    * 1x Circuito Integrado MAX232.
    * 2x Circuito Integrado L293D (Ponte H).
    * 1x Regulador de Tensão LM317 e 1x LM7805.
    * 1x Módulo de Rádio NRF24L01+.
    * Resistores, capacitores, LEDs e conectores diversos.
    * 1x Bateria recarregável.
* **Sistema de Visão:**
    * 1x Smartphone com sistema Android.
    * Aplicativo DroidCam (versão para Android e cliente para Windows/Linux).
* **Sistema de Controle:**
    * 1x Módulo de Rádio NRF24L01+ conectado a um computador via adaptador USB.

### Métodos

O desenvolvimento do projeto seguiu as etapas metodológicas adaptadas da proposta inicial:

1.  **Projeto Mecânico e Eletrônico:** A estrutura do robô foi modelada em software CAD e fabricada em acrílico. A PCB foi projetada para integrar de forma compacta o microcontrolador, o driver dos motores e o módulo de comunicação.

2.  **Montagem e Integração:** As partes mecânicas e eletrônicas foram montadas. Os motores foram acoplados ao chassi e conectados à PCB, que por sua vez foi energizada pela bateria.

3.  **Programação do Firmware:** Foi desenvolvido um firmware em linguagem C para o microcontrolador PIC. Este software é responsável por receber os comandos de movimento (ex: frente, trás, girar) via rádio frequência e acionar os motores correspondentemente através da ponte H L293D.

4.  **Configuração da Comunicação:** O sistema de comunicação sem fio foi estabelecido entre o robô e um computador. Um script de controle em Python foi desenvolvido no computador para enviar pacotes de dados para o robô através de um segundo módulo NRF24L01+.

5.  **Implementação do Sistema de Visão:** O aplicativo DroidCam foi instalado em um smartphone, e o cliente foi configurado no computador. O smartphone foi posicionado para capturar uma visão do campo de testes. O DroidCam então transmitia o vídeo em tempo real via Wi-Fi para o computador, que o reconhecia como um dispositivo de webcam padrão, tornando-o compatível com bibliotecas de visão computacional como o OpenCV.

## Resultados

O projeto culminou na construção bem-sucedida de um protótipo de robô totalmente funcional.

**Diagrama Final do Protótipo:**
O sistema final consiste em um robô autônomo cuja eletrônica é centralizada na PCB customizada. O microcontrolador PIC16F873a atua como o cérebro, recebendo dados do módulo de rádio NRF24L01+ e controlando as duas pontes H L293D, que por sua vez acionam os quatro motores. A alimentação é fornecida por uma bateria e regulada para as diferentes tensões necessárias no circuito. Externamente, o sistema de controle em um PC envia comandos, e o sistema de visão com DroidCam fornece o feedback visual do ambiente.

**Descrição dos Testes Realizados:**
Foram realizados testes incrementais para validar cada subsistema:
1.  **Teste de Locomoção:** Comandos básicos (andar para frente, para trás, rotação horária e anti-horária) foram enviados ao robô para verificar a resposta dos motores e a lógica de controle. O protótipo demonstrou capacidade de se mover conforme o esperado.
2.  **Teste de Comunicação:** Foi medido o alcance e a latência da comunicação via rádio frequência. O sistema se mostrou confiável dentro de uma área de 10 metros, adequada para um campo de VSS.
3.  **Teste de Integração de Visão:** O stream de vídeo do DroidCam foi aberto com sucesso no computador utilizando um script em Python com a biblioteca OpenCV. Foi possível capturar frames em tempo real, validando a solução como uma entrada viável para um futuro software de processamento de imagem.

**Apresentação e Análise dos Resultados:**
O robô construído atendeu aos requisitos fundamentais de locomoção e comunicação. A utilização do DroidCam provou ser uma alternativa extremamente eficaz e de baixo custo às câmeras industriais, permitindo a visualização em tempo real do protótipo em seu ambiente. Embora a taxa de quadros e a resolução sejam inferiores às de uma solução profissional, elas são suficientes para o desenvolvimento e teste de algoritmos de rastreamento de objetos em trabalhos futuros.

*[Inserir aqui Foto do robô finalizado]*

*[Inserir aqui Foto da PCB montada]*

*[Inserir aqui uma Tabela Comparativa: Características Propostas vs. Características Alcançadas]*

## Conclusão

Conclui-se que o objetivo principal do projeto foi alcançado com sucesso. Foi desenvolvido um protótipo de robô para futebol, validando os conceitos de modelagem mecânica, implementação eletrônica e comunicação sem fio. A adaptação do sistema de visão para utilizar o DroidCam representou uma contribuição significativa, demonstrando que é possível criar um ambiente de desenvolvimento completo para futebol de robôs com recursos acessíveis.

### Dificuldades Encontradas

* **Complexidade do Escopo:** O plano original de construir uma equipe de seis robôs mostrou-se excessivamente ambicioso para o tempo disponível, levando à decisão de focar em um único protótipo de alta qualidade.
* **Fabricação da PCB:** O processo de corrosão e soldagem dos componentes em uma placa de design compacto exigiu precisão e múltiplas tentativas para evitar curtos-circuitos e garantir a continuidade de todas as trilhas.
* **Configuração do Ambiente:** A instalação e configuração das bibliotecas de software (OpenCV, PySerial) e dos drivers para a comunicação entre o PC e o módulo de rádio apresentaram desafios de compatibilidade.
* **Calibração do DroidCam:** Encontrar o posicionamento ideal do smartphone para obter uma visão clara do campo, sem distorções e com boa iluminação, foi um processo de tentativa e erro.

### Sugestões para Trabalhos Futuros

* **Expansão da Equipe:** Construção dos robôs restantes para formar uma equipe completa, permitindo o desenvolvimento de estratégias de jogo em equipe.
* **Desenvolvimento do Software de IA:** Criar o software de visão computacional que utilize o stream do DroidCam para rastrear o robô, a bola e os adversários, e implementar uma máquina de estados ou algoritmos de inteligência artificial para a tomada de decisão autônoma.
* **Estrutura de Câmera Dedicada:** Projetar e construir um suporte elevado e estável para o smartphone, garantindo uma visão "top-down" padronizada do campo de jogo.
* **Upgrade de Hardware:** Migrar a plataforma do microcontrolador para uma mais moderna, como um ESP32, que já possui Wi-Fi integrado, podendo simplificar a arquitetura de comunicação e permitir o controle direto do robô pela rede local, eliminando a necessidade dos módulos NRF24L01+.

## Referências

* DEVCENTER. **DroidCam**. Disponível em: https://www.dev47apps.com/. Acesso em: 14 jul. 2025.
* GRUPO DE PESQUISA EM ROBÓTICA (GPR-UFS). **Caboclinhos - IEEE VSS**. Universidade Federal de Sergipe. Disponível em: [Inserir o link da página oficial do projeto Caboclinhos, se encontrar]. Acesso em: 14 jul. 2025.

```