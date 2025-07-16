# Título do Trabalho
**Futebol de Robôs: Modelagem, Implementação e Adaptação Estratégica**

## Introdução

No crescente campo da robótica e inteligência artificial, as competições acadêmicas servem como um catalisador para a inovação e o aprendizado prático. O futebol de robôs, especificamente na categoria VSS (Very Small Size), representa um desafio multidisciplinar que integra engenharia mecânica, eletrônica de precisão e software complexo. Este trabalho documenta a jornada de desenvolvimento de um protótipo para esta categoria, partindo de um objetivo ambicioso: a construção de uma equipe completa de seis robôs autônomos.

O plano original previa um sistema sofisticado com controle centralizado, comunicação sem fio e visão computacional para a coordenação em tempo real. No entanto, o percurso do projeto foi marcado por desafios pragmáticos, como restrições de financiamento e obstáculos logísticos, que exigiram uma reavaliação estratégica. O foco foi, então, redirecionado para a construção e validação de um único robô, mas com um nível de excelência que comprovasse a viabilidade de todo o conceito. Uma das principais inovações decorrentes dessa adaptação foi a implementação do sistema de visão, que substituiu câmeras industriais de alto custo por uma solução criativa e acessível: um smartphone com o aplicativo DroidCam. Esta abordagem não apenas viabilizou o projeto, mas também demonstrou um caminho alternativo e de baixo custo para o desenvolvimento e teste de sistemas robóticos complexos.

## Revisão da Literatura

A fundação teórica e prática deste projeto foi o trabalho da equipe **"Caboclinhos"**, do Grupo de Pesquisa em Robótica (GPR) da Universidade Federal de Sergipe (UFS). O acesso irrestrito ao seu repositório no GitHub foi um recurso inestimável. A arquitetura dos "Caboclinhos" é um exemplo de excelência na categoria VSS, baseada em três pilares:

1.  **Visão Computacional Global:** Utiliza uma única câmera posicionada acima do campo para capturar uma visão completa do jogo, permitindo que o software tenha conhecimento total da posição de todos os robôs (aliados e oponentes) e da bola.
2.  **Inteligência Centralizada:** As decisões estratégicas não são tomadas individualmente pelos robôs. Em vez disso, um computador central processa as informações da câmera, executa algoritmos de inteligência artificial para definir táticas e envia comandos de baixo nível (velocidade e direção) para cada robô via rádio.
3.  **Design Mecânico Robusto:** Os robôs são projetados para máxima agilidade, com sistemas de tração omnidirecional ou diferencial otimizados para aceleração rápida e manobras precisas.

O presente trabalho se diferencia por sua abordagem focada. Em vez de replicar a complexidade de uma equipe inteira, ele funciona como uma **prova de conceito**, validando os subsistemas mais críticos (locomoção, controle e comunicação) em um único protótipo. A adaptação mais significativa foi no pilar da visão computacional, onde a solução com DroidCam, embora com menor performance que uma câmera industrial, provou ser perfeitamente adequada para o desenvolvimento, calibração e teste de algoritmos, estabelecendo um framework de desenvolvimento de baixo custo.

## Materiais e Métodos

### Materiais

A lista de materiais a seguir representa o planejamento completo do projeto para a construção da equipe e da arena, conforme a proposta inicial.

| Item | Descrição | Unidade | Quantidade |
| :--- | :--- | :--- | :--- |
| 01 | Peças de acrílico para o chassi | unidade | 6 |
| 02 | Rodas de alto desempenho | unidade | 12 |
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

### Métodos de Execução

A metodologia real foi um processo iterativo de fabricação, montagem e teste, focado na construção de um protótipo e seu ambiente de controle.

**1. Fabricação do Chassi do Robô**
O processo iniciou com a modelagem das peças do chassi em software CAD, baseando-se no design do "Caboclinhos". Os arquivos de vetor foram então levados à **máquina de corte a laser do IFSC**. No software da máquina, foram configurados os parâmetros de potência e velocidade ideais para o corte de acrílico de 3mm. Após o ciclo de corte, as peças foram removidas e passaram por um acabamento manual para remover a película de proteção e limpar as arestas, resultando em um kit de montagem com encaixes perfeitos.

`[INSERIR IMAGEM AQUI: Foto da máquina de corte a laser do IFSC em operação, com o laser visível sobre a chapa de acrílico.]`
`[INSERIR IMAGEM AQUI: Foto das peças do chassi em acrílico, já cortadas e dispostas lado a lado antes da montagem para mostrar o resultado do corte.]`

**2. Fabricação da Placa de Circuito Impresso (PCB)**
Esta foi uma das etapas mais técnicas. O layout do circuito foi finalizado e exportado em arquivos Gerber, que foram utilizados na **fresadora CNC do IFSC**. O processo envolveu:
* **Usinagem:** A placa de fibra de vidro virgem foi fixada na mesa da CNC. A máquina executou o primeiro passe com uma fresa de ponta fina (V-bit) para criar o isolamento entre as trilhas de cobre.
* **Furação:** Com a troca da ferramenta para uma broca de diâmetro apropriado, a CNC realizou todas as furações dos componentes com extrema precisão.
* **Soldagem Manual:** Com a placa usinada em mãos, a soldagem foi um trabalho meticuloso. Utilizando uma estação de solda com controle de temperatura, solda fina e fluxo, cada componente foi posicionado e soldado, com atenção especial aos pinos do microcontrolador para evitar curtos.

`[INSERIR IMAGEM AQUI: Close-up da fresadora CNC do IFSC usinando as trilhas na placa de fibra de vidro.]`
`[INSERIR IMAGEM AQUI: Foto da placa de circuito impresso finalizada, com todos os componentes eletrônicos já soldados, mostrando a qualidade da soldagem.]`

**3. Construção do Campo de Jogo Oficial**
A criação de um ambiente de teste padronizado foi um subprojeto em si. O campo foi construído seguindo rigorosamente as dimensões e marcações estipuladas pelo regulamento oficial da liga IEEE Very Small Size Soccer.
* **Marcenaria de Precisão:** Utilizando uma chapa de MDF como base, as bordas foram cortadas e fixadas. A técnica de **escariação** foi aplicada com uma broca específica para que os parafusos ficassem perfeitamente nivelados com a superfície.
* **Acabamento Profissional:** Toda a superfície foi cuidadosamente preparada. Os furos dos parafusos foram cobertos com massa para madeira. Em seguida, múltiplas etapas de lixamento, com lixas de diferentes gramaturas, foram realizadas para criar uma base perfeitamente lisa e uniforme, essencial para o movimento do robô.
* **Pintura e Demarcação:** O campo recebeu uma camada de tinta verde fosca. As linhas (grande área, círculo central, etc.) foram demarcadas com fita de vinil branca, cortada e aplicada com precisão milimétrica conforme o livro de regras.

`[INSERIR IMAGEM AQUI: Foto do campo em MDF durante a fase de construção, mostrando o processo de lixamento, pintura ou aplicação das fitas de marcação.]`
`[INSERIR IMAGEM AQUI: Foto panorâmica do campo de jogo finalizado, com todas as marcações visíveis e o gol posicionado.]`

**4. Desenvolvimento do Firmware e Software**
O cérebro do robô foi programado no **MPLAB X IDE** com o compilador **XC8**. O código em C foi desenvolvido para inicializar os periféricos do PIC16F873a (timers para PWM, comunicação serial) e entrar em um loop principal. Neste loop, ele constantemente verifica a chegada de um novo pacote de dados do rádio NRF24L01+. Ao receber um comando, o firmware o decodifica e traduz em sinais PWM que são enviados às pontes H L293D, controlando a velocidade e a direção de cada motor individualmente.

**5. Implementação do Sistema de Visão**
A solução de visão foi implementada estabelecendo uma conexão de rede (via Wi-Fi ou USB tethering) entre o smartphone executando o DroidCam (servidor) e o PC com o cliente DroidCam. Este cliente cria um driver de câmera virtual no sistema operacional. Dessa forma, qualquer software no PC, incluindo o script Python desenvolvido para o projeto, pode acessar o vídeo do celular como se fosse uma webcam padrão, simplesmente chamando a função `cv2.VideoCapture(index)` da biblioteca OpenCV.

`[INSERIR IMAGEM AQUI: Foto da montagem física do sistema de visão, mostrando o smartphone posicionado em um suporte sobre o campo de jogo.]`

## Cronograma Planejado

O cronograma a seguir detalha o planejamento original das atividades do projeto. É importante notar que o cronograma real sofreu alterações significativas devido aos desafios de financiamento e logística detalhados na seção de dificuldades.

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

## Resultados

O projeto resultou em um ecossistema de hardware e software funcional e validado.

**Protótipo Final e Ambiente de Testes:**
O robô finalizado demonstrou uma locomoção ágil e responsiva no campo de MDF construído, respondendo aos comandos enviados pelo computador com latência mínima. A integração do sistema de visão com DroidCam foi um sucesso, fornecendo um stream de vídeo estável (640x480 a 30fps) ao software de controle, confirmando-o como uma entrada de dados viável para algoritmos de processamento de imagem em tempo real. Para os testes, foi utilizada uma bola de ping-pong laranja, que possui o mesmo diâmetro de 40mm especificado pela regra, servindo como uma substituta adequada para fins de desenvolvimento.

`[INSERIR IMAGEM AQUI: Foto principal do protótipo do robô totalmente montado, em destaque no campo de jogo.]`
`[INSERIR IMAGEM AQUI: Captura de tela do software de controle no PC, exibindo a janela com o vídeo ao vivo do DroidCam.]`

## Conclusão

Este projeto, embora redimensionado de sua concepção original, alcançou com sucesso seu objetivo fundamental: validar uma arquitetura completa para futebol de robôs. Foi desenvolvido um protótipo robusto, desde a fabricação digital do chassi e da PCB até a programação do firmware. A superação de desafios pragmáticos através de soluções criativas, como o uso do DroidCam, não diminuiu o projeto, mas sim enriqueceu a experiência de aprendizado, provando que é possível engajar em pesquisa e desenvolvimento em robótica de ponta com recursos acessíveis. O trabalho estabelece uma base sólida e bem documentada para futuras expansões.

### Dificuldades Encontradas

* **Captação de Recursos e Escopo:** O projeto foi concebido com a expectativa de verba de um projeto de fomento submetido ao IFSC. A não aprovação do financiamento foi o principal obstáculo, forçando uma readequação completa do escopo de uma equipe de seis robôs para um único protótipo, executado com recursos próprios.

* **Atrasos Logísticos em Cascata:** O cronograma foi duplamente impactado. A espera pela resposta do projeto de fomento consumiu a fase inicial de planejamento. Subsequentemente, quando a compra de materiais foi iniciada, uma greve dos Correios causou atrasos imprevisíveis e longos na entrega de componentes essenciais, comprimindo drasticamente o tempo disponível para montagem e teste.

* **Engenharia Reversa e Adaptação Eletrônica:** A documentação do projeto de referência, embora boa, possuía lacunas, especialmente na PCB. Foi necessário realizar um trabalho de engenharia reversa, usando um multímetro e estudando os datasheets dos componentes para mapear todas as conexões antes da soldagem. A maior adaptação foi na placa de transmissão, cujo conector de alimentação teve de ser completamente redesenhado para se adequar a um componente diferente do original.

* **Desafios de Montagem e Componentes:** A materialização do projeto encontrou barreiras na aquisição de peças. Parafusos com as dimensões exatas do projeto original não foram encontrados, forçando a adaptação do chassi. A busca por uma bateria de Lítio (LiPo) de 7.4V e 2C com as dimensões exatas para caber no espaço exíguo do chassi foi particularmente difícil e demorada.

* **Construção Manual do Campo:** A construção do campo de MDF, apesar do resultado satisfatório, foi um processo manual complexo que demandou uma variedade de ferramentas de marcenaria e experiência prévia com esse tipo de trabalho. Interpretar o regulamento oficial da liga IEEE Very Small Size Soccer para transpor todas as marcações para o campo com precisão milimétrica foi uma tarefa particularmente trabalhosa e detalhista.

### Sugestões para Trabalhos Futuros

* **Desenvolvimento do Software de IA:** Utilizar a base de hardware e visão estabelecida para criar o software de processamento de imagem que, usando OpenCV, identifique as cores do robô, da bola e do campo, e implemente uma máquina de estados para controle autônomo.
* **Upgrade de Hardware:** Migrar a plataforma do microcontrolador para uma mais moderna, como um ESP32, que já possui Wi-Fi integrado, podendo simplificar a arquitetura de comunicação e permitir o controle direto do robô pela rede local.
* **Refinamento Mecânico:** Projetar e implementar um mecanismo de chute para o robô, adicionando uma nova dimensão de jogabilidade.

## Unidades Curriculares Envolvidas

O conhecimento adquirido em diversas disciplinas do curso foi fundamental para o sucesso deste projeto:

-   **Programação 1 e 2:** Essencial para desenvolver a lógica de controle no firmware do robô em C e os scripts de teste no computador em Python.
-   **Eletrônica 1 e 2:** Aplicada no entendimento de circuitos, na função da ponte H para controle de motores, nos reguladores de tensão e no projeto geral da PCB.
-   **Microcontroladores:** Conhecimento central para a programação do PIC, configuração de registradores, interrupções e periféricos como PWM e comunicação serial.
-   **Sistemas de Comunicação:** Forneceu a base para entender e implementar a comunicação sem fio com os módulos de rádio NRF24L01+.
-   **Desenho Técnico:** Habilidade utilizada na modelagem CAD do chassi do robô para o corte a laser.
-   **Física 1 (Fundamentos de Mecânica):** Conhecimentos aplicados na análise intuitiva da dinâmica, estabilidade e tração do robô.
-   **Instrumentação Eletrônica:** Relevante para os processos de depuração e teste dos circuitos eletrônicos com o uso de multímetro.

## Referências

* GRUPO DE PESQUISA EM ROBÓTICA (GPR-UFS). **Caboclinhos - Repositório Oficial**. GitHub. Disponível em: https://github.com/GPRUFS/Caboclinhos/tree/main. Acesso em: 14 jul. 2025.
* DEVCENTER. **DroidCam**. Disponível em: https://www.dev47apps.com/. Acesso em: 14 jul. 2025.
* IEEE ROBOTICS AND AUTOMATION SOCIETY. **RoboCupSmall Size League Rules**. Disponível em: [Inserir link oficial das regras, ex: https://sslrules.robocup.org/]. Acesso em: 14 jul. 2025.
* [Adicionar outras referências de vídeos e sites consultados, se houver].