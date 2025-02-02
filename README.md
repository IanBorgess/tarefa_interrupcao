# Projeto de Controle de Matriz de LEDs com Raspberry Pi Pico

Este projeto utiliza um Raspberry Pi Pico para controlar uma matriz de LEDs, permitindo a exibição de diferentes padrões através da interação com dois botões. O código foi desenvolvido em C/C++ utilizando o SDK do Raspberry Pi Pico.

## Descrição do Projeto

O projeto consiste em uma matriz de LEDs que exibe diferentes desenhos pré-configurados. Dois botões são utilizados para navegar entre os desenhos: um botão para avançar e outro para retroceder. Além disso, um LED pisca continuamente para indicar que o sistema está em funcionamento.

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
  - `pisca_led()`: Faz o LED piscar.
  - `interrupcao()`: Função de interrupção que detecta o pressionamento dos botões.
  - `main()`: Função principal que inicializa o sistema e gerencia a exibição dos padrões na matriz de LEDs.

## Como Funciona

1. **Inicialização**: O sistema é inicializado configurando os pinos do LED e dos botões. A matriz de LEDs é configurada e o primeiro padrão é exibido.

2. **Interrupções**: Quando um botão é pressionado, uma interrupção é gerada, e a função `interrupcao()` é chamada para atualizar o estado dos botões.

3. **Navegação entre Padrões**: No loop principal, o LED pisca continuamente. Se um botão for pressionado, o contador de padrões é incrementado ou decrementado, e o novo padrão é exibido na matriz de LEDs.

## Como Usar

1. **Hardware Necessário**:
   - Raspberry Pi Pico
   - Matriz de LEDs
   - Dois botões
   - Resistores e jumpers

2. **Compilação e Upload**:
   - Utilize o ambiente de desenvolvimento compatível com o Raspberry Pi Pico (como o Visual Studio Code com a extensão Pico SDK).
   - Compile o código e faça o upload para o Raspberry Pi Pico.

3. **Execução**:
   - Após o upload, o sistema iniciará automaticamente.
   - Pressione os botões para navegar entre os diferentes padrões exibidos na matriz de LEDs.

## Exemplo de Uso

- **Botão A**: Avança para o próximo padrão na matriz.
- **Botão B**: Retrocede para o padrão anterior na matriz.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests para melhorar o projeto.

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
