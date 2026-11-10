# 🔐 Brute Force com Medusa e Kali Linux

Projeto prático desenvolvido durante o Bootcamp Santander Cibersegurança — DIO  
Simulação de ataque de força bruta em ambiente controlado e isolado.

## ⚠️ Aviso Legal

Este projeto foi desenvolvido exclusivamente em ambiente virtual isolado, para fins educacionais.  
Nunca utilize estas técnicas em sistemas sem autorização explícita. 
Testes de invasão sem permissão são ilegais.

## 🎯 Objetivo

Demonstrar como ataques de força bruta funcionam na prática, utilizando a ferramenta Medusa contra um ambiente vulnerável controlado (Metasploitable 2).

## 🧰 Ferramentas e Ambiente

| Ferramenta | Função |

| Oracle VirtualBox | Virtualização das máquinas |
| Kali Linux | Sistema do atacante |
| Metasploitable 2 | Sistema-alvo (vulnerável) |
| Medusa | Ferramenta de brute force |
| Nmap | Enumeração de portas e serviços |

## 🏗️ Configuração do Ambiente

### Topologia de Rede

Ambas as VMs configuradas com adaptador Host-Only no VirtualBox, garantindo isolamento total da rede real.

[ Kali Linux ]  <---(Host-Only Network)--->  [ Metasploitable 2 ]
192.168.56.103                               192.168.56.103
(atacante)                                        (alvo)

### Pré-requisitos

- VirtualBox instalado
- Kali Linux importado
- Metasploitable 2 importado
- Ambas as VMs no mesmo adaptador Host-Only

## 🗂️ Wordlist Utilizada

Arquivo: `wordlist.txt`

## ⚔️ Ataque: Força Bruta em FTP

### Reconhecimento (Nmap)

Comando utilizado para identificar serviços ativos no alvo:

nmap -sV 192.168.56.103

### Execução do Ataque (Medusa)

medusa -h 192.168.56.103 -u msfadmin -P wordlist.txt -M ftp

**Explicação de cada parâmetro:**

| Parâmetro | Significado |

| `-h` | IP do host alvo |
| `-u` | Usuário único a testar |
| `-P` | Arquivo com lista de senhas |
| `-M ftp` | Módulo do protocolo alvo |

### Resultado

📚 O que Aprendi

Esta jornada prática me permitiu aprender a executar ataques de força bruta utilizando o Medusa no Kali Linux e o ambiente Metasploitable 2. Me fez  compreender a lógica operacional de comprometimento de credenciais, a criação de wordlists e desenvolver uma visão crítica indispensável sobre segurança corporativa. Além da técnica, consolidou o entendimento de que algumas ferramentas clássicas continuam essenciais mesmo na era da Inteligência Artificial. 

---

## 👤 Autor

JOSÉ ALBERTO DE OLIVEIRA SILVA 
[LinkedIn](www.linkedin.com/in/alberto-oliveira-5587b3446)
[GitHub](https://github.com/ALBERTO-CYBERAPC)
