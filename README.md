<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=02A6F4&height=120&section=header"/>
<h1 align="center">Embarcatech Atividade - U4C8 </h1>

## Objetivo do Projeto


O objetivo deste projeto é utilizar o conversor analógico-digital (ADC) do microcontrolador RP2040 para ler a posição de um joystick, controlando a intensidade de dois LEDs RGB por meio de PWM com base nessas leituras. Além disso, a posição do joystick será representada em um display SSD1306, utilizando o protocolo I2C para comunicação.

## 🗒️ Lista de requisitos

- **Uso de interrupções**: Todas as funcionalidades relacionadas aos botões devem ser implementadas utilizando rotinas de interrupção (IRQ); 
- **Debouncing**: É obrigatório implementar o tratamento do bouncing dos botões via software; 
- **Utilização do Display 128 x 64**: A utilização de fontes maiúsculas e minúsculas demonstrará o domínio do uso de bibliotecas, o entendimento do princípio de funcionamento do display, bem como, a utilização do protocolo I2C.
- **Envio de informação pela UART**: Visa observar a compreensão sobre a comunicação serial via UART. 
- **Organização do código**: O código deve estar bem estruturado e comentado para facilitar o entendimento.

## 🛠 Tecnologias

- **Microcontrolador:** Raspberry Pi Pico W  
- **LEDs:** RGB (Vermelho, Verde, Azul)  
- **Botão A**: Conectado à GPIO 5.  
- **Display SSD1306**: Conectado via I2C (GPIO 14 e GPIO15).
- **Botão do Joystick**: conectado à GPIO 22.
- **Joystick**: conectado aos GPIOs 26 e 27.    
- **Linguagem de Programação:** C  
- **Frameworks:** Pico SDK


## 🔧 Funcionalidades Implementadas:

1. **Controle de Intensidade dos LEDs RGB com Joystick**

- O eixo Y do joystick controla a intensidade do LED Azul: valores menores no eixo Y aumentam o brilho do LED Azul, enquanto valores maiores diminuem a intensidade. O LED estará apagado quando o joystick estiver na posição central (valor 2048).
- O eixo X do joystick controla a intensidade do LED Vermelho: valores menores no eixo X aumentam o brilho do LED Vermelho, enquanto valores maiores diminuem a intensidade. O LED estará apagado quando o joystick estiver na posição central (valor 2048).
- A variação de brilho dos LEDs será feita via PWM, permitindo um ajuste suave da intensidade luminosa de ambos os LEDs.
- Exibição da Posição do Joystick no Display SSD1306
- Um quadrado de 8x8 pixels será exibido no display SSD1306, com sua posição sendo atualizada de acordo com os valores dos eixos X e Y do joystick. O quadrado se moverá proporcionalmente às variações dos valores capturados pelo joystick, proporcionando uma visualização gráfica da posição.
- Interação com o Botão do Joystick, em que a pressionar o botão do joystick alternará o estado do LED Verde, ligando-o ou desligando-o a cada acionamento.
- O botão também modificará a borda do display SSD1306 a cada acionamento, alternando entre diferentes estilos de borda, indicando que o botão foi pressionado.
- Pressionar o botão A ativará ou desativará o controle PWM dos LEDs. Isso permitirá alternar entre a funcionalidade de controle de brilho dos LEDs e a desativação dessa funcionalidade, oferecendo mais flexibilidade na operação do sistema.

## 🚀 Passos para Compilação e Upload  

1. **Clonar o repositório** 

- sh
- git clone seu repositorio


2. **Configurar e compilar o projeto**  

`mkdir build && cd build`
`cmake ..`
`make`

3. **Transferir o firmware para a placa**

- Conectar a placa BitDogLab ao computador
- Copiar o arquivo .uf2 gerado para o drive da placa

4. **Testar o projeto**

🛠🔧🛠🔧🛠🔧


## 🎥 Demonstração: 

- Para ver o funcionamento do projeto, acesse o vídeo de demonstração gravado por José Vinicius em: https://youtu.be/YmlDdGBSoDU

## 💻 Desenvolvedor
 
<table>
  <tr>
    <td align="center"><img style="" src="https://avatars.githubusercontent.com/u/191687774?v=4" width="100px;" alt=""/><br /><sub><b> José Vinicius </b></sub></a><br />👨‍💻</a></td>
  </tr>
</table>
