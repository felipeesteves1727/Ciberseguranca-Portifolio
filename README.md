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

SYN
↓
SYN + ACK
↓
ACK
