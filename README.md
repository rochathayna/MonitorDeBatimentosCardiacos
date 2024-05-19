# MonitorDeBatimentosCardiacos
Este repositório contém o código-fonte de um projeto desenvolvido para monitorar os batimentos cardíacos usando um dispositivo ESP8266 e enviar os dados para um servidor MQTT.

# Monitor de Batimentos Cardíacos com ESP8266 e MQTT

Este projeto consiste em um monitor de batimentos cardíacos que utiliza um dispositivo ESP8266 para ler os batimentos cardíacos de um sensor de pulso, exibir as leituras em um display OLED e enviar os dados para um servidor MQTT. Ele também inclui a integração com o aplicativo MQTTBox para visualização e análise dos dados em tempo real.

## Componentes Utilizados

- ESP8266: O microcontrolador Wi-Fi utilizado para a leitura dos batimentos cardíacos e comunicação MQTT.
- Sensor de Pulso: Um sensor conectado ao ESP8266 para detectar os batimentos cardíacos.
- LED e Buzzer: Utilizados para fornecer feedback visual e sonoro ao usuário.
- Display OLED: Utilizado para exibir as leituras dos batimentos cardíacos localmente.

## Contribuição

Contribuições são bem-vindas! Se você encontrar problemas ou tiver sugestões de melhorias, sinta-se à vontade para abrir um problema ou enviar um pull request.

## Interfaces, Protocolos e Módulos de Comunicação

O monitor de batimentos cardíacos utiliza o protocolo MQTT para comunicação com um servidor MQTT. Ele também utiliza a biblioteca Adafruit_SSD1306 para controle do display OLED e as funções padrão da Arduino IDE para controle dos pinos GPIO e comunicação serial.


