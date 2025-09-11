# TCC – Sistema de Gerenciamento de Dispositivos Inteligentes com Home Assistant

Este repositório contém os arquivos e configurações utilizadas no Trabalho de Conclusão de Curso (TCC) sobre a implementação de um sistema inteligente baseado no Home Assistant.

## 🔧 Tecnologias utilizadas

- Home Assistant
- Node-RED
- Grafana
- InfluxDB
- ESPHome
- MQTT
- Câmeras ONVIF
- **Frigate** (NVR com detecção de objetos via IA)

## 📁 Estrutura do projeto

- `/node-red/`: Fluxos exportados do Node-RED em JSON
- `/homeassistant/`: Arquivo de configuração `configuration.yaml`
- `/grafana/`: Dashboards utilizados para monitoramento
- `/frigate/`: Configuração do Frigate (`config.yml`) e instruções de uso
- `/docs/`: Tutoriais de instalação e configuração
- `/testes/`: Resultados e imagens capturadas

## 📌 Reprodutibilidade

Todos os arquivos estão disponíveis para replicação do ambiente. Siga o passo a passo no arquivo [`docs/tutorial_instalacao.md`](docs/tutorial_instalacao.md)

## 📸 Capturas de tela

![Home Assistant](imagens/home_assistant.png)  
![Node-RED](imagens/node_red.png)

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
