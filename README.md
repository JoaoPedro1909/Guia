# Guia de Implantação - Módulo Web Servidor Industrial Mineral

## 1. Visão Geral
O módulo web do **Servidor Industrial Mineral** tem como propósito monitorar e gerenciar em tempo real os dados de produção mineral de plantas industriais.  
Permite registro de extração, rastreamento de transporte, geração de relatórios e integração com sistemas ERP industriais e sensores IoT.

---

## 2. Pré-requisitos
- **Software e Ferramentas Necessárias:**
  - PHP >= 7.4
  - MySQL >= 8.0
  - Node.js >= 16
  - Composer
  - Nginx ou Apache
- **Versões Mínimas Recomendadas:**
  - Laravel 8.x
  - Vue.js 3.x
- **Acesso e Permissões Necessárias:**
  - Acesso SSH ao servidor de produção
  - Permissões de leitura/escrita nas pastas de logs e storage
  - Acesso ao broker MQTT para integração com sensores

---

## 3. Especificações Técnicas
- **Arquitetura:**
  - Sistema em 3 camadas:
    - Frontend Vue.js
    - Backend Laravel PHP
    - Banco MySQL
  - Comunicação com sensores IoT via protocolo MQTT

- **Tecnologias:**
  - **Linguagens:** PHP, JavaScript
  - **Banco de dados:** MySQL 8
  - **Bibliotecas e Frameworks:**
    - Laravel 8
    - Vue.js 3
    - Mosquitto MQTT Client

- **Configurações:**
  - **Variáveis de ambiente:**
    - `APP_ENV=production`
    - `DB_HOST=127.0.0.1`
    - `MQTT_BROKER_URL=mqtt://broker.mineral.local`
  - **Parâmetros de conexão:**
    - Usuário e senha do banco configurados no `.env`
    - Porta padrão MQTT: 1883

---

## 4. Procedimento Padrão de Registro de Implantação
1. **Registro de data e horário:**
   - Ex.: 2025-07-01 10:30
2. **Nome e função do responsável pela implantação:**
   - Ex.: Ana Souza, Engenheira de Software
3. **Máquina ou servidor alvo:**
   - VPS Ubuntu 20.04 - IP: 192.168.1.100
4. **Versão do artefato implantado:**
   - v1.0.0
5. **Comentários e observações:**
   - Implantação inicial do módulo web de monitoramento.

---

## 5. Checklist de Implantação
- [x ] Planejamento concluído
- [x ] Ambiente preparado
- [x ] Deploy executado
- [ x] Testes de validação realizados
- [x ] Logs revisados

---

## 6. Validação e Testes
Após o deploy, realizar os seguintes testes:

- **Testes de carga:**
  - Simulação de 50 usuários simultâneos acessando dashboards.
- **Testes funcionais:**
  - Criação de registros de produção.
  - Geração de relatórios.
  - Visualização em tempo real de sensores.
- **Testes de integração:**
  - Verificar recebimento dos dados via MQTT.
  - Conferir atualização automática dos indicadores.

---

## 7. Avaliação e Feedback
- **Problemas e soluções adotadas:**
  - Ex.: Erro de permissão em diretório `storage` solucionado com `chmod -R 775`.
- **Sugestões de melhoria:**
  - Automatizar execução de testes pós-deploy.
  - Adicionar monitoramento via Prometheus.

---

## 8. Anexos

- **Scripts de configuração:**
  - `scripts/install_dependencies.sh`
  - `scripts/setup_env.sh`

- **Modelos de relatórios:**
  - Relatório Diário de Produção
  - Relatório de Performance dos Sensores
