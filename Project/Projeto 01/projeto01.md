# Gerenciando Instâncias EC2 na AWS

---

## Descrição do Desafio
Este projeto foi desenvolvido como parte do bootcamp, tendo como foco a criação de um diagrama arquitetural no Draw.io para representar o funcionamento do Gerador de Relatórios na AWS.
A proposta do desafio foi aplicar na prática os conceitos de gerenciamento de instâncias EC2, armazenamento em nuvem com o Amazon S3 e automação de tarefas com o AWS Lambda, consolidando o aprendizado sobre os principais serviços da Amazon Web Services.

A arquitetura criada ilustra como esses serviços se integram para processar dados e gerar relatórios automaticamente, simulando um fluxo real dentro do ecossistema AWS.
O resultado é um repositório que documenta de forma visual e organizada o funcionamento desse sistema, servindo como base para estudos e futuras implementações.

---

## Visão Geral dos Serviços Utilizados

### Amazon EC2 (Elastic Compute Cloud)

O Amazon EC2 é um serviço de computação em nuvem que permite criar e gerenciar instâncias virtuais (servidores) para hospedar aplicações, executar processos e realizar tarefas sob demanda.
No contexto deste projeto, a EC2 representa o componente responsável pela execução principal das operações de processamento dentro do sistema Gerador de Relatórios.

### Amazon S3 (Simple Storage Service)

O Amazon S3 é um serviço de armazenamento de objetos altamente escalável e seguro, utilizado para guardar arquivos, dados e backups.
No projeto, ele atua como o repositório central onde os arquivos e dados necessários para gerar os relatórios são armazenados e organizados.

### AWS Lambda

O AWS Lambda permite executar funções de forma automática e sem servidor (serverless), em resposta a eventos dentro da AWS.
No Gerador de Relatórios, ele é o componente que automatiza o fluxo de processamento, sendo acionado sempre que um novo arquivo é enviado ao S3, gerando relatórios de forma dinâmica e eficiente.

---

## Arquitetura Criada
A arquitetura desenvolvida segue o diagrama abaixo:

![Fluxograma](https://i.imgur.com/PB6oc8w.jpeg)

---

### Explicação da Arquitetura

O diagrama desenvolvido representa:

- Uma instância EC2 responsável pela execução principal dos processos;
- Um bucket S3 destinado ao armazenamento e manipulação dos arquivos utilizados nos relatórios;
- Uma função AWS Lambda acionada automaticamente por eventos do S3, responsável por processar dados e gerar relatórios;
- O fluxo de comunicação entre os serviços, mostrando de forma clara como o sistema se comporta dentro do ambiente AWS.

---

### Tecnologias Utilizadas

- **Draw.io** – Criação do diagrama arquitetural
- **Amazon EC2** – Hospedagem e execução de processos
- **Amazon S3** – Armazenamento de arquivos e dados
- **AWS Lambda** – Automação e processamento sem servidor

---

## Resultados e Aprendizados

Durante o desenvolvimento deste projeto, foi possível:

- Explorar na prática o papel das instâncias EC2 em ambientes de computação em nuvem;
- Entender a importância do S3 como repositório seguro e escalável;
- Aplicar conceitos de automação utilizando funções Lambda;
- Criar uma visão clara e documentada de todo o fluxo de geração de relatórios na nuvem.
