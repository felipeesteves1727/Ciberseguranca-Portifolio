# 🔎 Wireshark Network Traffic Analysis

## 📌 Introdução

Este projeto apresenta uma análise de tráfego de rede realizada utilizando o Wireshark.

O objetivo foi observar, na prática, diferentes etapas da comunicação de rede, analisando consultas DNS, estabelecimento de conexões TCP e início de uma comunicação protegida por TLS.

## 🎯 Objetivos

- Analisar tráfego de rede
- Identificar protocolos de comunicação
- Analisar consultas DNS
- Observar o estabelecimento de conexões TCP
- Identificar endereços IP e portas
- Observar o início de uma conexão TLS
- Documentar os resultados utilizando evidências reais

## 🛠️ Ferramenta utilizada

- Wireshark

## 🌐 Conceitos analisados

- DNS
- UDP
- TCP
- TCP Three-Way Handshake
- TLS 1.3
- HTTPS
- Endereçamento IP
- Portas de comunicação

---

# 🔬 Análises realizadas

## 1. Análise DNS

Foi identificada uma consulta DNS para:

`clientservices.googleapis.com`

A comunicação observada apresentou:

- **Origem:** `192.168.18.10`
- **Destino:** `192.168.18.1`
- **Protocolo:** UDP
- **Porta de destino:** 53

A análise demonstra uma consulta DNS realizada pelo computador para o servidor DNS da rede.

### 📸 Evidência

![DNS Query](./screenshots/01-dns-query.png)

---

## 2. Análise do TCP Three-Way Handshake

Foi observada uma sequência de estabelecimento de conexão TCP composta por três etapas:

```text
SYN
↓
SYN + ACK
↓
ACK
DNS
 ↓
TCP
 ↓
TLS 1.3
 ↓
Comunicação protegida
- **Origem:** `192.168.18.10`
- **Destino:** `192.168.18.1`
- **Protocolo:** UDP
- **Porta de destino:** 53

A análise demonstra uma consulta DNS realizada pelo computador para o servidor DNS da rede.

### 📸 Evidência

![DNS Query](./screenshots/01-dns-query.png)

---

## 2. Análise do TCP Three-Way Handshake

Foi observada uma sequência de estabelecimento de conexão TCP composta por três etapas:

```text
SYN
↓
SYN + ACK
↓
ACK
---

## 3. Análise TLS 1.3

Foi observado um pacote TLS 1.3 do tipo:

`Client Hello`

A comunicação observada apresentou:

- **Origem:** `192.168.18.10`
- **Destino:** `52.123.244.228`
- **Porta de origem:** 54202
- **Porta de destino:** 443
- **Protocolo:** TLS 1.3
- **SNI:** `ecs.office.com`

O Client Hello representa o início da negociação TLS observada na captura.

### 📸 Evidência

![TLS 1.3 Client Hello](./screenshots/03-tls-client-hello.png)

---

# 📊 Resultados

Durante o laboratório foi possível observar uma sequência de comunicação envolvendo diferentes protocolos:

```text
DNS
 ↓
TCP
 ↓
TLS 1.3
 ↓
Comunicação protegida
