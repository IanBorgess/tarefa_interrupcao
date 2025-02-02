# Projeto de Controle de Matriz de LEDs com Interrupções e Debouncing

Este projeto utiliza um Raspberry Pi Pico para controlar uma matriz de LEDs, permitindo a exibição dos números de 0 a 9 através da interação com dois botões. Link para o vídeo a seguir:

[Clique aqui para ver o vídeo do projeto](https://youtube.com/shorts/A-6HVkjLbcQ?feature=share).

## Descrição do Projeto

O projeto consiste em uma matriz de LEDs que exibe os números de 0 a 9 na matriz de leds WS2812. Dois botões são utilizados para navegar entre os desenhos: um botão para avançar e outro para retroceder. Além disso, um LED pisca continuamente em vermelho para indicar que o sistema está em funcionamento.

## Estrutura do Código

O código está organizado da seguinte forma:

- **Inclusão de Bibliotecas**: São incluídas as bibliotecas necessárias para controlar o hardware do Raspberry Pi Pico, como `pico/stdlib.h`, `hardware/pio.h`, e uma biblioteca personalizada `matriz_leds.h`.

- **Definições e Variáveis Globais**:
  - `LED_RED`: Pino onde o LED está conectado.
  - `button_A` e `button_B`: Pinos onde os botões estão conectados.
  - `matriz0` a `matriz9`: Matrizes que definem os padrões de LEDs a serem exibidos.
  - `matriz[]`: Array de ponteiros para as matrizes de padrões.
  - `botaoA` e `botaoB`: Variáveis booleanas para detectar o pressionamento dos botões.

- **Funções**:
  - `setup()`: Configura os pinos do LED e dos botões.
  - `pisca_led()`: Faz o LED piscar 5x por segundo na cor vermelha.
  - `interrupcao()`: Função de interrupção que detecta o pressionamento dos botões e faz o debouncing.
  - `main()`: Função principal que inicializa o sistema e gerencia a exibição dos padrões na matriz de LEDs.

## Exemplo de Uso

- **Botão A**: Avança para o próximo padrão na matriz.
- **Botão B**: Retrocede para o padrão anterior na matriz.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests para melhorar o projeto.

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
