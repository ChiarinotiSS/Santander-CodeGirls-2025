# Gerenciando Instâncias EC2 na AWS

---

## Descrição
Este projeto foi desenvolvido durante o bootcamp com o objetivo de representar graficamente a arquitetura do sistema Gerador de Relatórios, utilizando o Draw.io.
A proposta consiste em demonstrar a integração entre os serviços Amazon EC2, Amazon S3 e AWS Lambda, simulando o fluxo de processamento e geração automatizada de relatórios na nuvem.

---

## Descrição do Desafio
Este laboratório tem como objetivo consolidar os conhecimentos em **gerenciamento de instâncias EC2** na AWS.  
O entregável consiste em um repositório organizado contendo anotações, diagramas e insights obtidos durante a prática.

---

## Objetivo
Consolidar os conhecimentos sobre instâncias EC2, armazenamento em nuvem e funções serverless, aplicando conceitos teóricos em um modelo visual e prático de arquitetura AWS.

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

## Tecnologias Utilizadas

**Draw.io** – Criação do diagrama arquitetural
**Amazon EC2** – Hospedagem e execução de processos
**Amazon S3** – Armazenamento de arquivos e dados
**AWS Lambda** – Automação e processamento sem servidor

---

## Resultados e Aprendizados

Durante o desenvolvimento deste projeto, foi possível:

- Explorar na prática o papel das instâncias EC2 em ambientes de computação em nuvem;
- Entender a importância do S3 como repositório seguro e escalável;
- Aplicar conceitos de automação utilizando funções Lambda;
- Criar uma visão clara e documentada de todo o fluxo de geração de relatórios na nuvem.
