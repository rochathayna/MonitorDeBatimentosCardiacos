# Documentação do Projeto

## Descrição do funcionamento
Este código implementa um monitor de batimentos cardíacos usando um microcontrolador ESP8266, um sensor de pulso e um display OLED. O código lê os batimentos cardíacos do sensor de pulso, exibe a taxa de batimentos no display OLED e fornece feedback sonoro e visual por meio de um buzzer e um LED.

O código consiste em um loop principal que verifica se um dedo está sobre o sensor de pulso. Quando um dedo é detectado, o código realiza as seguintes etapas:

### Leitura dos Batimentos Cardíacos
O sensor de pulso é lido usando a função analogRead(PULSE_SENSOR_PIN), e o valor é comparado com o limiar definido em PULSE_THRESHOLD para determinar se um dedo está presente.

### Feedback Sonoro e Visual
Se um dedo estiver presente, um som é emitido pelo buzzer usando a função tone(BUZZER_PIN, 500) com uma frequência de 500Hz. Além disso, o LED é piscado ligando e desligando o pino definido em LED_PIN.

### Exibição da Taxa de Batimentos
A taxa de batimentos é calculada mapeando o valor lido do sensor de pulso para a faixa desejada (50 a 90 batimentos por minuto). A taxa de batimentos é então exibida no display OLED com a função display.print(bpm).

### Atualização do Display
O display é atualizado com as informações da taxa de batimentos e mantido ligado até que o dedo seja removido do sensor.

### Hardware Utilizado
ESP8266: Microcontrolador Wi-Fi usado para o processamento e comunicação.
Sensor de Pulso: Sensor utilizado para detectar os batimentos cardíacos.
Display OLED: Display utilizado para exibir a taxa de batimentos cardíacos.
Buzzer e LED: Componentes utilizados para fornecer feedback sonoro e visual.

### Configurações de Hardware
BUZZER_PIN: Pino utilizado para controlar o buzzer.
LED_PIN: Pino utilizado para controlar o LED.
PULSE_SENSOR_PIN: Pino de entrada utilizado para conectar o sensor de pulso.
PULSE_THRESHOLD: Limiar para detectar a presença do dedo sobre o sensor de pulso.

### Bibliotecas Utilizadas
Wire.h: Biblioteca para comunicação I2C.
Adafruit_GFX.h: Biblioteca para gráficos vetoriais.
Adafruit_SSD1306.h: Biblioteca para controle do display OLED.

## Para Reproduzir
# Instalação e Uso

1. Clone ou faça o download deste repositório.
3. Conecte o ESP8266 ao computador via USB e carregue o código para o dispositivo.
4. Conecte o sensor de pulso ao ESP8266 de acordo com o esquema de pinagem definido no código.
5. Certifique-se de configurar corretamente o nome da rede Wi-Fi e a senha no código.
6. Configure um servidor MQTT e atualize o código com as informações de conexão.
7. Inicie a monitoração dos batimentos cardíacos e visualize os dados no display OLED.
8. Utilize o aplicativo MQTTBox para se conectar ao servidor MQTT e visualizar os dados em tempo real.

## Contribuição

Contribuições são bem-vindas! Se você encontrar problemas ou tiver sugestões de melhorias, sinta-se à vontade para abrir um problema ou enviar um pull request.


