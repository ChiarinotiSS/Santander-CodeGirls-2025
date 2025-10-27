# AWS Step Functions: Orquestração de Workflows

Durante esta fase do meu aprendizado em computação em nuvem, aprofundei meus estudos sobre orquestração de microserviços utilizando o AWS Step Functions.  
A experiência foi extremamente valiosa para compreender como diferentes serviços podem trabalhar em conjunto dentro de um workflow automatizado e totalmente serverless.

---

## Conceitos Fundamentais Aplicados

Durante a implementação, explorei conceitos importantes relacionados a arquiteturas modernas e baseadas em eventos:

### Arquitetura de Microserviços
- **Desacoplamento:** cada função Lambda realiza uma tarefa isolada.  
- **Escalabilidade:** os serviços podem crescer de forma independente.  
- **Resiliência:** falhas em um componente não interrompem o sistema inteiro.

### AWS Step Functions
- Serviço de **orquestração de workflows**, ideal para coordenar múltiplos serviços AWS em um fluxo centralizado.  
- Permite criar fluxos visuais e declarativos, integrando serviços como **Lambda**, **SNS**, **SQS** e **DynamoDB**.

#### Tipos de estados suportados:
- **Task:** executa uma função Lambda ou integração direta.  
- **Choice:** implementa decisões condicionais.  
- **Pass:** transmite dados sem executar código.  
- **Wait:** insere atrasos controlados no fluxo.  
- **Succeed / Fail:** finalizam o workflow com sucesso ou erro, respectivamente.

### Amazon SNS e SQS

- **Amazon SNS (Simple Notification Service):**
  - Envia notificações para múltiplos assinantes simultaneamente.  
  - Ideal para comunicação baseada em eventos.

- **Amazon SQS (Simple Queue Service):**
  - Garante entrega assíncrona de mensagens entre sistemas.  
  - Mantém o desacoplamento e resiliência de aplicações distribuídas.

###  Amazon ECS e EKS

- **Amazon ECS (Elastic Container Service):**
  - Serviço de orquestração de containers nativo da AWS.  
  - Permite execução em **AWS Fargate (serverless)** ou **EC2**.

- **Amazon EKS (Elastic Kubernetes Service):**
  - Solução gerenciada de **Kubernetes** na AWS.  
  - Ideal para equipes que já utilizam Kubernetes e desejam escalar seus clusters na nuvem.

---

## Conclusão

Com o AWS Step Functions, compreendi na prática como automatizar e orquestrar processos complexos que envolvem múltiplos serviços AWS.  
Essa abordagem facilita a criação de soluções modulares, resilientes e escaláveis, reduzindo o esforço de integração manual e aumentando a eficiência de todo o sistema.

---

## Exemplo de Código (Lambda - Node.js)

Abaixo, um exemplo simplificado de função Lambda que pode ser utilizada dentro de um workflow para consultar o preço de uma ação e gerar uma recomendação automática:

```javascript
const AWS = require('aws-sdk');

// Exemplo de função Lambda para simular decisão de compra/venda
exports.handler = async (event) => {
  const stockPrice = event.price || 100;
  const threshold = 120;

  const recommendation =
    stockPrice < threshold ? "buy" : "sell";

  console.log(`Preço da ação: ${stockPrice} → Recomendação: ${recommendation.toUpperCase()}`);

  return {
    statusCode: 200,
    body: JSON.stringify({
      stockPrice,
      recommended_type: recommendation,
      message: `Ação recomendada: ${recommendation}`
    }),
  };
};
