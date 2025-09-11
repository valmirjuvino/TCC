# 🛠️ Tutorial de Instalação do Sistema Inteligente com Home Assistant

Este guia explica como instalar e configurar todos os componentes utilizados no projeto TCC.

---

## 1. Pré-requisitos

- Servidor com **Proxmox** instalado
- Acesso à internet
- Conhecimentos básicos em redes e Linux

---

## 2. Instalação do Home Assistant

1. Criar uma VM no Proxmox com 2 GB de RAM e 32 GB de disco.
2. Baixar a imagem `.qcow2` do Home Assistant: https://www.home-assistant.io/installation/linux
3. Importar a imagem no Proxmox com o comando:
   ```bash
   qm importdisk 101 home_assistant.qcow2 local-lvm
   ```
4. Iniciar a VM e acessar via navegador:
   ```
   http://IP_DO_SERVIDOR:8123
   ```

---

## 3. Instalar o Node-RED (via Add-on)

1. Acesse `http://IP_DO_HOME_ASSISTANT:8123`
2. Vá em **Supervisor > Add-ons > Node-RED**
3. Instale e inicie o serviço

---

## 4. Instalar o Grafana + InfluxDB

1. Instale ambos via Add-ons ou Docker
2. Configure a base de dados `home_assistant`
3. Crie painéis com as métricas desejadas

---

## 5. Configuração do MQTT

1. Instale o **Mosquitto Broker**
2. Crie um usuário no Home Assistant
3. Edite o `configuration.yaml`:
   ```yaml
   mqtt:
     broker: 192.168.100.3
     username: valmir
     password: SUA_SENHA
   ```

---

## 6. Integração de Dispositivos

- **Tuya:** via HACS com autenticação local
- **Câmeras ONVIF:** Adicione via interface de integrações
- **ESPHome:** Compile e envie via USB ou OTA

---

## 7. Fluxos Node-RED

Importe o JSON disponível na pasta `/node-red/` para replicar as automações.

---

## 8. Configuração do Frigate (Detecção de Objetos)

1. Instale o Frigate via LXC ou Docker
2. Configure as câmeras no arquivo `config.yml`
3. Use RTSP e ONVIF

---

## 🔁 Reprodutibilidade

Todos os arquivos estão disponíveis neste repositório. Basta seguir este passo a passo e importar as configurações para ter um ambiente funcional.

---

## 📬 Suporte

Dúvidas? Entre em contato com:
**Valmir Juvino da Silva**