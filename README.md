# ESP32 + MQTT (HiveMQ)

Projeto simples para conectar um **ESP32** ao broker MQTT do HiveMQ e controlar um LED.

---

# Login no HiveMQ

- Acesse o site:
   https://www.hivemq.com/mqtt-cloud-broker/

- Crie sua conta ou faça login.

---

# Criar um Cloud (Cluster)

- Clique em **Create Cluster**
- Escolha o plano **Free**

Após criar, vá na aba **Overview** e terá um URL parecido com esse:

```
ae2f5769cb3f469ea0f3fa274d5adb40.s1.eu.hivemq.cloud
```

Esse será o **endereço do seu broker MQTT**.

---

# Criar usuário e senha

- Vá em **Access Management**
- Clique em **Credentials**
- Clique em **Add Credentials**
- Crie um usuário e senha para conectar ao MQTT.

Exemplo usado no projeto:

```
Username: SENAI_IOT01_web_client
Password: Aa123456789
```

---

# Conectar no Web Client

Após criar as credenciais:

1. Vá na aba **Web Client**
2. Clique em **Connect**

---

# Tópicos MQTT

Controle do LED:

```
Led1IotSenai
```

Publicação de dados do sensor:

```
Sensor1IotSenai
```

---

# Funcionamento

1. O ESP32 conecta ao WiFi
2. Conecta ao broker MQTT do HiveMQ
3. Escuta o tópico `Led1IotSenai`
4. Se receber `ON` ou `1`, o LED liga
5. Se receber `OFF` ou `0`, o LED desliga

