💧 Sistema de Irrigação Automática com IoT e MQTT

Este repositório apresenta um projeto de automação de irrigação utilizando ESP32, sensor de umidade e comunicação com broker MQTT via Wi-Fi.

🔧 Componentes utilizados

ESP32

Sensor de umidade do solo (analógico)

LED (simulando a bomba d'água)

Plataforma de simulação: Wokwi

Protocolo de comunicação: MQTT (test.mosquitto.org)

Biblioteca: PubSubClient


🧠 Lógica de funcionamento

O ESP32 conecta-se à rede Wi-Fi.

Lê os dados do sensor de umidade conectado ao pino 34.

Publica o valor lido em irrigacao/umidade.

Caso a umidade esteja abaixo de um limite (ex: <900), o LED é acionado simulando o funcionamento da bomba, e uma mensagem é enviada para irrigacao/status.

Caso contrário, o LED permanece desligado.


📡 Tópicos MQTT utilizados

irrigacao/umidade (publicação do valor do sensor)

irrigacao/status (status da bomba)


📂 Estrutura do repositório

├── main.ino               # Código-fonte principal com Wi-Fi e MQTT
├── diagrama_fritzing.png  # Imagem do circuito simulado
├── grafico_tempo.png      # Gráfico com tempo de resposta
├── README.md              # Este arquivo

📺 Observação sobre simulação

O simulador Wokwi não permite conexão MQTT real, mas o código está funcional e pronto para ser utilizado em um ESP32 real. No ambiente físico, o dispositivo se conecta normalmente ao broker test.mosquitto.org.

🎥 Demonstração em vídeo

Assista à demonstração no YouTube: https://youtu.be/FwXNnHz7s3c

🧠 Autores

Matheus Miguel Abreu da Silva, Gustavo Mezei Silva


---

Faculdade de Computação e Informática - Universidade Presbiteriana Mackenzie
