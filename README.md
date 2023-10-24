# Explorando as Interfaces de Comunicação do Raspberry Pi Pico W: Manual de Referência, Características e Prova de Conceito

*Cristiane de Andrade Coutinho*
*Instituto de Tecnologia e Liderança INTELI*
*Ciência da Computação*
*23/10/2023*

## RESUMO

O **Raspberry Pi Pico W**, baseado no chip **RP2040**, é uma placa microcontroladora flexível e acessível que opera a 2,4 GHz. O manual de referência da Raspberry Pi Foundation oferece detalhes técnicos, ambiente de desenvolvimento e design físico. Com um processador ARM Cortex-M0+ dual-core de até 133 MHz, 16 MB de memória flash e 26 pinos GPIO programáveis, suporta interfaces como UART, SPI e I2C, além de ambientes como o Raspberry Pi Pico C/C++ SDK e MicroPython. Uma prova de conceito simples demonstra o controle de um LED com a interface GPIO, alternando-o a cada meio segundo. Essas informações destacam as capacidades e versatilidade do Raspberry Pi Pico W em sistemas embarcados.

## 1 MANUAL DE REFERÊNCIA DO COMPONENTE

O **Raspberry Pi Pico W** é uma placa microcontroladora que utiliza o chip **RP2040** da Raspberry Pi como núcleo. Ele foi concebido como uma plataforma de desenvolvimento de custo acessível e altamente flexível para o RP2040, operando na frequência de 2,4 GHz.

Para entender as especificações técnicas e funcionalidades do **Raspberry Pi Pico W**, foi consultado o manual de referência oficial da Raspberry Pi Foundation. Este documento fornece informações abrangentes sobre o dispositivo, incluindo:

### Especificações Técnicas:

- O **Raspberry Pi Pico W** é baseado no microcontrolador **RP2040**, que é equipado com um processador **ARM Cortex-M0+ dual-core** com uma frequência de operação de até **133 MHz**.
- Possui **16 MB** de memória flash, **26 pinos GPIO** programáveis e suporte a diversas interfaces de comunicação, como **UART**, **SPI**, **I2C**, **PWM**, entre outras.
- O dispositivo inclui módulos para gerenciamento de temporização, interrupções e energia.

### Ambiente de Desenvolvimento:

- O **Raspberry Pi Pico W** pode ser programado com o **Raspberry Pi Pico C/C++ SDK**, que inclui bibliotecas e ferramentas de desenvolvimento.
- Também é compatível com o ambiente **MicroPython**, que é uma implementação do Python otimizada para dispositivos microcontroladores.
- A programação pode ser feita via USB ou através de um programador externo.

  O **Raspberry Pi Pico W** foi projetado para fornecer um circuito externo mínimo, mas altamente flexível, que suporta o chip **RP2040**. Este circuito inclui componentes essenciais, como memória flash **Winbond W25Q16JV**, um cristal, fontes de alimentação e desacoplamento, bem como um conector USB.
  A maioria dos pinos do microcontrolador **RP2040** é roteada para os pinos de E/S do usuário, localizados nas bordas esquerda e direita da placa. Quatro desses pinos são dedicados a funções internas, incluindo o acionamento de um LED, o controle da energia da fonte de alimentação no modo de comutação integrado (SMPS) e a detecção de tensões do sistema.
   Além disso, o **Raspberry Pi Pico W** é equipado com uma interface sem fio de 2,4 GHz integrada, utilizando o módulo **Infineon CYW43439**. A antena é uma unidade integrada licenciada pela **ABRACON** (anteriormente conhecida como **ProAnt**). A interface wireless está conectada ao **RP2040** através da interface **SPI**.
   O design do **Pico W** foi concebido para acomodar conectores de pinos soldados de 0,1 polegada (com um passo de 0,1 polegada mais largo do que um pino padrão de 40 pinos em embalagem DIP). Ele também pode ser usado como um 'módulo' montável em superfície, uma vez que os pinos de E/S do usuário são montados na placa. Adicionalmente, existem pads **SMT** (Tecnologia de Montagem em Superfície) localizados abaixo do conector USB e do botão **BOOTSEL**, permitindo o acesso a esses sinais quando o **Pico W** é usado como um módulo **SMT** soldado por refluxo.

## 2 INTERFACES DE COMUNICAÇÃO COM O COMPONENTE

O **Raspberry Pi Pico W** é rico em interfaces de comunicação, proporcionando versatilidade em aplicações de sistemas embarcados:

### UART (Universal Asynchronous Receiver/Transmitter):

- A **UART** é uma interface de comunicação serial assíncrona.
- É adequada para conectar dispositivos que requerem comunicação serial, como sensores, displays, GPS e outros microcontroladores.
- Oferece taxas de transferência configuráveis e permite a transmissão e recepção de dados.

### SPI (Serial Peripheral Interface):

- A **SPI** é uma interface síncrona que facilita a comunicação com dispositivos periféricos, como sensores, displays e memórias.
- Ela opera em modo mestre/escravo e utiliza um barramento comum para transferência de dados.
- Oferece alta velocidade de comunicação e suporte a diferentes modos de operação.

### I2C (Inter-Integrated Circuit):

- A **I2C** é uma interface de comunicação serial de dois fios que permite a conexão eficiente de vários dispositivos em um único barramento.
- É amplamente usada para sensores, memórias EEPROM, acelerômetros e outros dispositivos de baixa velocidade.
- Cada dispositivo possui um endereço único no barramento I2C.

## 3 PROVA DE CONCEITO

**Controlando um LED com o Raspberry Pi Pico W**:

### Objetivo:

Demonstrar como controlar um LED usando a interface GPIO do **Raspberry Pi Pico W** com **wokwi**. Nesta prova de conceito, o objetivo é acionar um LED e fazer com que ele pisque, desligando a cada meio segundo.

### Materiais Necessários:

- **Raspberry Pi Pico W**
- Um LED
- Um resistor de **220Ω** (ou próximo)
- Jumpers/fios para conexão

O LED conectado ao Raspberry Pi Pico W deve começar a piscar, indicando que o controle da interface GPIO foi bem-sucedido. Esta é uma prova de conceito simples que demonstra como usar um dos recursos mais básicos do Raspberry Pi Pico W. Você pode expandir e personalizar essa prova de conceito, adicionando mais LEDs, sensores ou até mesmo controlando o LED com base em informações de sensores, para criar projetos mais avançados.
Para avaliação, o projeto se encontra nesse link: https://wokwi.com/projects/379435702519184385

## 6 CONCLUSÃO

Este relatório proporcionou uma caracterização completa do Raspberry Pi Pico W, incluindo o manual de referência do componente, a descrição das interfaces de comunicação e uma prova de conceito detalhada que demonstra a utilização prática da interface UART para a comunicação com outro sistema. Essas informações são essenciais para desenvolvedores e entusiastas que desejam explorar as capacidades do Raspberry Pi Pico W em aplicações de sistemas embarcados.

## REFERÊNCIAS

- [https://www.makerhero.com/produto/raspberry-pi-pico-w/](https://www.makerhero.com/produto/raspberry-pi-pico-w/)
- [https://datasheets.raspberrypi.com/picow/pico-w-datasheet.pdf?_gl=1*f1ezc9*_ga*MTQxNTk1NTk3MC4xNjk4MDc8tjv8tuub8gthibsl2w42b8msh2gvb2aw] (https://datasheets.raspberrypi.com/picow/pico-w-datasheet.pdf?_gl=1*f1ezc9*_ga*MTQxNTk1NTk3MC4xNjk4MDc8tjv8tuub8gthibsl2w42b8msh2gvb2aw)
