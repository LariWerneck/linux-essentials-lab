# Linux Essentials Lab – Prática com Docker

Este repositório documenta a prática realizada durante o laboratório de Linux Essentials utilizando Docker.

A atividade foi baseada no repositório: https://github.com/marialazara/linux-essentials

This repository is available in Portuguese (PT), English (EN), and French (FR).

Ce projet est documenté en portugais, anglais et français afin d’assurer l’accessibilité à un public plus large.

## 🛠 Ambiente utilizado
```bash
# Baixar a imagem do laboratório
docker pull marialazaradev/linux-essentials:latest

# Executar o container
docker run -it --name devops-investigation marialazaradev/linux-essentials:latest
```

----

## 🎯 Introdução ao Cenário
### Contexto Empresarial
A **MariaLazaraCloud** é uma empresa de tecnologia que oferece soluções SaaS B2B para automação de cobrança e faturamento. A arquitetura usa microserviços em containers Docker, com foco em disponibilidade.

### O Incidente
**Data/Hora:** 27 de setembro de 2024, 14:25 UTC  
**Serviço Afetado:** billing-api (API de pagamentos)  
**Sintomas Iniciais:**
- Aplicação não processa transações
- Erros de corrupção de dados nos logs
- Falha na validação de integridade
- Serviço rodando, mas rejeitando transações
- Dashboard em "degraded"

### Seu Papel
Você é o DevOps Engineer on-call. Como o sistema é legado e tem pouca documentação, você não conhece bem os caminhos dos arquivos. Vamos explorar o sistema calmamente, usando comandos básicos como `find` apenas quando necessário para localizar arquivos e diretórios. Cada passo inclui explicações detalhadas dos comandos (o que cada parte faz), e reflexões sobre por quê usá-los, quando aplicá-los, o motivo e o objetivo. Assumimos que você é iniciante no Linux, então vamos devagar, com narrativas explicando o que estamos fazendo antes de prosseguir para o próximo passo.

----

## 📚 O que pratiquei

- Navegação no sistema de arquivos Linux
- Análise de processos ativos
- Monitoramento de logs em tempo real (tail -f)
- Investigação de erros utilizando grep
- Busca de arquivos com find
- Manipulação de arquivos e diretórios (cp, mv, mkdir, chmod)
- Edição de arquivos com nano
- Aplicação de troubleshooting estruturado
- Conceitos de ambiente produtivo e rollback

----

## 🖥️ Navegação e Sistema

### Comandos essenciais praticados:

- pwd        | mostra diretório atual
- whoami     | mostra usuário atual
- uname -a   | informações completas do sistema
- ls -la     | lista arquivos e detalhes
- cd         | navegação entre diretórios

### Estrutura importante do Linux:

- / → diretório raiz
- /home → usuários comuns
- /root → usuário root
- /var/log → arquivos de log do sistema

----

## 📊 Monitoramento de Recursos
- df -h      | espaço em disco
- free -h    | memória
- ps aux     | processos ativos

### Filtrando processos:
- ps aux | grep billing

----

## 📂 Manipulação de Arquivos
- touch arquivo.txt        | cria arquivo
- mkdir pasta              | cria diretório
- cp origem destino        | copia arquivos
- mv origem destino        | move/renomeia
- diff arq1 arq2           | compara diferenças
- chmod 644 arquivo.sh     | altera permissões

----

## 📝 Logs e Monitoramento em Tempo Real

### Logs geralmente localizados em:
- /var/log

### Principais comandos:
- head arquivo.log         | primeiras linhas
- tail arquivo.log         | últimas linhas
- tail -f arquivo.log      | monitoramento em tempo real
- cat arquivo.log          | exibe conteúdo completo

### Filtrando erros:
- tail arquivo.log | grep "ERROR"

----

## 🔎 Localização de Arquivos
- find / -name "billing" | Busca arquivos ou diretórios pelo nome a partir da raiz.

----

## ✍️ Edição no Linux
- nano arquivo.txt | Editor direto no terminal para ajustes rápidos em ambiente de servidor.




# 🇺🇸 Linux Essentials Lab – Practice with Docker

This repository documents the practice carried out during the Linux Essentials lab using Docker.

The activity was based on the repository: https://github.com/marialazara/linux-essentials

## 🛠 Environment Used
```bash
# Pull the lab image
docker pull marialazaradev/linux-essentials:latest

# Run the container
docker run -it --name devops-investigation marialazaradev/linux-essentials:latest
```

----

## 🎯 Scenario Introduction
### Business Context
**MariaLazaraCloud** is a technology company that provides B2B SaaS solutions for billing and invoicing automation. The architecture uses Docker container-based microservices, focusing on availability.

### The Incident
**Date/Time:** September 27, 2024, 14:25 UTC
**Affected Service:** billing-api (payment API)
**Initial Symptoms:**
- Application not processing transactions
- Data corruption errors in logs
- Integrity validation failure
- Service running but rejecting transactions
- Dashboard in "degraded" state

### Your Role
You are the on-call DevOps Engineer. Since the system is legacy and poorly documented, you are not familiar with the file paths. We will explore the system calmly, using basic commands like `find` only when necessary to locate files and directories. Each step includes detailed explanations of the commands (what each part does), and reflections on why to use them, when to apply them, the reason, and the objective. We assume you are a Linux beginner, so we proceed carefully, explaining what we are doing before moving to the next step.

----

## 📚  What I Practiced

- Navigating the Linux file system
- Analyzing active processes
- Monitoring logs in real time (tail -f)
- Investigating errors using grep
- Searching files with find
- Managing files and directories (cp, mv, mkdir, chmod)
- Editing files with nano
- Applying structured troubleshooting
- Production environment and rollback concepts

----

## 🖥️ Navigation and System

### Essential commands practiced:

- pwd | shows current directory
- whoami | shows current user
- uname -a | complete system information
- ls -la | lists files and details
- cd | directory navigation

### Important Linux structure:

- / → root directory
- /home → regular users
- /root → root user
- /var/log → system log files

----

## 📊 Resource Monitoring
- df -h      | disk space
- free -h    | memory
- ps aux     | active processes

Filtering processes:
- ps aux | grep billing

----

## 📂 File Management
- touch file.txt | creates file
- mkdir folder | creates directory
- cp source destination | copies files
- mv source destination | moves/renames
- diff file1 file2 | compares differences
- chmod 644 file.sh | changes permissions

----

## 📝 Logs and Real-Time Monitoring

### Logs usually located in:
- /var/log

### Main commands:
- head file.log | first lines
- tail file.log | last lines
- tail -f file.log | real-time monitoring
- cat file.log | displays full content

### Filtering errors:
- tail arquivo.log | grep "ERROR"

----

## 🔎 File Location
- find / -name "billing" | Searches files or directories by name starting from root.

----

## ✍️ Editing in Linux
- nano file.txt | Terminal-based editor for quick adjustments on servers.


# 🇫🇷 Linux Essentials Lab – Pratique avec Docker

Ce dépôt documente la pratique réalisée pendant le laboratoire Linux Essentials en utilisant Docker.

L'activité était basée sur le dépôt : https://github.com/marialazaradev/linux-essentials

## 🛠 Environnement utilisé
```bash
# Télécharger l'image du laboratoire
docker pull marialazaradev/linux-essentials:latest

# Exécuter le conteneur
docker run -it --name devops-investigation marialazaradev/linux-essentials:latest
```

----

## 🎯 Introduction au Scénario
### Contexte de l'entreprise
**MariaLazaraCloud** est une entreprise technologique qui propose des solutions SaaS B2B pour l'automatisation de la facturation et du recouvrement. L'architecture utilise des microservices conteneurisés avec Docker, axés sur la disponibilité.

### L'Incident
**Date/Heure :** 27 septembre 2024, 14:25 UTC  
**Service affecté :** billing-api (API de paiement)  
**Symptômes initiaux :**
- L'application ne traite pas les transactions
- Erreurs de corruption de données dans les logs
- Échec de validation d'intégrité
- Service en cours d'exécution mais rejetant les transactions
- Tableau de bord en état "degraded"

### Votre rôle
Vous êtes l’ingénieur DevOps d’astreinte. Comme le système est ancien et peu documenté, vous ne connaissez pas bien les chemins des fichiers. Nous allons explorer le système calmement, en utilisant des commandes de base comme `find` uniquement lorsque nécessaire pour localiser des fichiers et répertoires. Chaque étape inclut des explications détaillées des commandes (ce que fait chaque partie), ainsi que des réflexions sur pourquoi les utiliser, quand les appliquer, la raison et l’objectif. Nous supposons que vous êtes débutant en Linux, donc nous avançons progressivement en expliquant ce que nous faisons avant de passer à l’étape suivante.

----

## 📚  Ce que j’ai pratiqué

- Navigation dans le système de fichiers Linux
- Analyse des processus actifs
- Surveillance des logs en temps réel (tail -f)
- Investigation des erreurs avec grep
- Recherche de fichiers avec find
- Manipulation de fichiers et répertoires (cp, mv, mkdir, chmod)
- Édition de fichiers avec nano
- Application d’un troubleshooting structuré
- Concepts d’environnement de production et rollback

----

## 🖥️ Navigation et Système

### Commandes essentielles pratiquées :

- pwd | affiche le répertoire actuel
- whoami | affiche l'utilisateur actuel
- uname -a | informations complètes du système
- ls -la | liste les fichiers et détails
- cd | navigation entre répertoires

### Structure Linux importante :

- / → répertoire racine
- /home → utilisateurs standards
- /root → utilisateur root
- /var/log → fichiers journaux système

----

## 📊 Surveillance des Ressources
- df -h | espace disque
- free -h | mémoire
- ps aux | processus actifs

Filtering processes:
- ps aux | grep billing

----

## 📂 Manipulation de Fichiers
- touch file.txt | crée un fichier
- mkdir folder | crée un répertoire
- cp source destination | copie des fichiers
- mv source destination | déplace/renomme
- diff file1 file2 | compare les différences
- chmod 644 file.sh | modifie les permissions

----

## 📝 Logs et Surveillance en Temps Réel

### Logs généralement situés dans :
- /var/log

### Commandes principales :
- head file.log | premières lignes
- tail file.log | dernières lignes
- tail -f file.log | surveillance en temps réel
- cat file.log | affiche le contenu complet

### Filtrer les erreurs :
- tail arquivo.log | grep "ERROR"

----

## 🔎 Localisation de Fichiers
- find / -name "billing" | Recherche des fichiers ou répertoires par nom à partir de la racine.

----

## ✍️ Édition sous Linux
- nano file.txt | Éditeur en terminal pour des ajustements rapides sur serveur.
