# Network Traffic Analysis with Wireshark
 
> Relatório técnico de análise de tráfego de rede utilizando Wireshark, desenvolvido como parte do **Google Cybersecurity Professional Certificate**.\
> Technical report on network traffic analysis using Wireshark, developed as part of the **Google Cybersecurity Professional Certificate**.
 
> **Idioma / Language:** [Português](#-português) · [English](#-english)
 
---
 
## Português
 
### Sobre o projeto
 
Este repositório contém um relatório de análise de tráfego de rede, no qual atuei como analista de segurança investigando o tráfego gerado durante o acesso a um site. A atividade foi realizada utilizando uma máquina virtual Windows fornecida pelo Qwiklabs, como parte prática do **Google Cybersecurity Professional Certificate**.
 
O objetivo central foi demonstrar competências fundamentais para profissionais de segurança da informação e redes: capturar, filtrar e interpretar pacotes de rede para identificar endereços, protocolos e dados transmitidos durante uma sessão de navegação.
 
### Objetivos da análise
 
- Identificar os endereços IP de origem e destino envolvidos em uma sessão de rede.
- Examinar os protocolos utilizados durante o estabelecimento de uma conexão com um site.
- Realizar uma análise detalhada de pacotes individuais para determinar o tipo de informação transmitida e recebida.
### Metodologia
 
A análise foi conduzida em etapas, utilizando um arquivo de captura de pacotes (`sample.pcap`) aberto no Wireshark:
 
1. **Exploração inicial da captura** — leitura das colunas padrão do Wireshark (Nº, Time, Source, Destination, Protocol, Length, Info) e identificação das regras de cores utilizadas para classificar pacotes (ex.: tráfego DNS, TCP/HTTP, ICMP).
2. **Inspeção de pacote individual** — análise das subcamadas de um pacote (Frame, Ethernet II, Internet Protocol v4, TCP), incluindo endereços MAC, IPs, portas e flags TCP.
3. **Filtragem por endereço IP** — aplicação de filtros como `ip.addr`, `ip.src` e `ip.dst` para isolar o tráfego relacionado a um host específico.
4. **Filtragem por endereço MAC** — uso do filtro `eth.addr` para localizar pacotes associados a uma interface de rede específica.
5. **Análise de tráfego DNS** — filtragem de pacotes UDP na porta 53 (`udp.port == 53`) para examinar consultas (queries) e respostas (answers) de resolução de nomes.
6. **Análise de tráfego TCP/HTTP** — filtragem da porta 80 (`tcp.port == 80`) e busca por conteúdo específico no payload (`tcp contains "curl"`).
### Competências demonstradas
 
- Captura e análise de tráfego de rede com Wireshark
- Leitura e interpretação de pacotes em múltiplas camadas (Ethernet, IP, TCP/UDP, DNS, HTTP, ICMP)
- Criação e aplicação de filtros de exibição (display filters)
- Identificação de endereços IP, MAC e portas em comunicações de rede
- Documentação técnica de processos de investigação de segurança
- Fundamentos práticos de análise forense de rede
### Conteúdo do repositório
 
| Arquivo | Descrição |
|---|---|
| [`Network_Traffic_Analysis_ENG.pdf`](Network_Traffic_Analysis_ENG.pdf) | Relatório completo em português |
| [`Network_Traffic_Analysis_ENG.pdf`](Network_Traffic_Analysis_ENG.pdf) | Relatório completo em inglês |
 
### Contexto da atividade
 
Este projeto faz parte do programa **Google Cybersecurity Professional Certificate**, oferecido na plataforma Coursera, e foi executado em um ambiente de laboratório virtual (Qwiklabs).
 
---
 
## English
 
### About the project
 
This repository contains a network traffic analysis report in which I acted as a security analyst investigating traffic generated during a website visit. The activity was performed on a Windows virtual machine provided by Qwiklabs, as a hands-on component of the **Google Cybersecurity Professional Certificate**.
 
The main goal was to demonstrate core competencies for information security and network professionals: capturing, filtering, and interpreting network packets to identify addresses, protocols, and transmitted data during a browsing session.
 
### Analysis objectives
 
- Identify the source and destination IP addresses involved in a network session.
- Examine the network protocols used while establishing a connection to a website.
- Perform an in-depth analysis of individual packets to determine the type of information transmitted and received.
### Methodology
 
The analysis was carried out step by step using a packet capture file (`sample.pcap`) opened in Wireshark:
 
1. **Initial exploration of the capture** — reviewing Wireshark's standard columns (No., Time, Source, Destination, Protocol, Length, Info) and identifying the coloring rules used to classify packets (e.g., DNS traffic, TCP/HTTP, ICMP).
2. **Single packet inspection** — analyzing a packet's layers (Frame, Ethernet II, Internet Protocol v4, TCP), including MAC addresses, IPs, ports, and TCP flags.
3. **Filtering by IP address** — applying filters such as `ip.addr`, `ip.src`, and `ip.dst` to isolate traffic related to a specific host.
4. **Filtering by MAC address** — using the `eth.addr` filter to locate packets associated with a specific network interface.
5. **DNS traffic analysis** — filtering UDP traffic on port 53 (`udp.port == 53`) to examine name resolution queries and answers.
6. **TCP/HTTP traffic analysis** — filtering port 80 (`tcp.port == 80`) and searching for specific payload content (`tcp contains "curl"`).
### Skills demonstrated
 
- Network traffic capture and analysis with Wireshark
- Reading and interpreting packets across multiple layers (Ethernet, IP, TCP/UDP, DNS, HTTP, ICMP)
- Building and applying display filters
- Identifying IP addresses, MAC addresses, and ports in network communications
- Technical documentation of security investigation processes
- Practical fundamentals of network forensic analysis
### Repository contents
 
| File | Description |
|---|---|
| [`Network_Traffic_Analysis__PTBR_.pdf`](Network_Traffic_Analysis__PTBR_.pdf) | Full report (Portuguese) |
| [`Network_Traffic_Analysis_ENG.pdf`](Network_Traffic_Analysis_ENG.pdf) | Full report (English) |
 
### Activity context
 
This project is part of the **Google Cybersecurity Professional Certificate** program on Coursera and was carried out in a virtual lab environment (Qwiklabs).
 
---
 
## Autor / Author
 
**GitHub:** [@surufel](https://github.com/surufel)
