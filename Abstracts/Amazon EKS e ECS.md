# ✨Amazon EKS✨

Serviço gerenciado que facilita a execução do Kubernetes na AWS, ele elimina a necessidade de instalar, operar e manter clusters Kubernetes manualmente, proporcionando um ambiente seguro, confiável e escalável para workloads em contêineres.

## 🌸Principais Características🌸
- **Execução simplificada do Kubernetes:** a AWS gerencia o plano de controle (control plane).
- **Escalonamento automático:** aumenta ou reduz recursos do cluster conforme a demanda.
- **Eficiência operacional:** ajusta dinamicamente o tamanho do cluster para rodar serviços de forma otimizada.
- **Integração AWS:** conecta-se a serviços como VPC, IAM, CloudWatch, Load Balancer etc.

## 🌸Quando usar o EKS?🌸
- Organizações que já utilizam Kubernetes ou querem adotá-lo.
- Times que precisam de portabilidade multi-cloud (Kubernetes roda em várias nuvens e on-premises).
- Ambientes complexos que exigem alta flexibilidade e padronização de orquestração.

---

# ✨Amazon ECS✨

Serviço gerenciado de orquestração de contêineres que permite executar, interromper e gerenciar contêineres em clusters na AWS. Suporta arquitetura de microserviços com escalabilidade, segurança e desempenho.

## 🌸Principais Características🌸
- **Gerenciamento simples:** automatiza a criação e manutenção de clusters.
- **Escalabilidade:** aumenta/diminui contêineres conforme a demanda.
- **Integração fácil:** funciona de forma nativa com IAM, VPC, CloudWatch etc.
- **Segurança:** aplicação de políticas de acesso e controle refinado.

## 🌸Microserviços em Contêineres🌸
- Cada parte do app (ex: catálogo, carrinho, pagamentos) roda em um contêiner Docker.
- Definição de Tarefas (container definitions) e Serviços ECS para manter disponibilidade.
- Auto Scaling: políticas para escalar automaticamente (ex: mais contêineres em promoções).
- Monitoramento & Logs: integração com CloudWatch para métricas e troubleshooting.

## 🌸Relação ECS x ECR🌸
- **ECS (Elastic Container Service):** orquestra e gerencia os contêineres.
- **Elastic Container Registry):** armazena e gerencia imagens Docker.

### 🌸Quando usar ECS?🌸
- Para tarefas de longa duração (mais de 15 minutos).
- Quando precisa executar código fora das regiões da AWS.
- Cenários que exigem personalização de rede, segurança e monitoramento.

---

## ✨Diferença ECS x EKS✨
- **ECS (nativo AWS):** simples, integrado, indicado para quem não precisa de Kubernetes.
- **EKS (Kubernetes gerenciado):** indicado para quem já domina Kubernetes ou quer portabilidade e padronização com clusters fora da AWS.

