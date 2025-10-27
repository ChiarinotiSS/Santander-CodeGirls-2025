# AWS CloudFormation

---

## O que é o AWS CloudFormation?

O AWS CloudFormation é um serviço da Amazon Web Services que permite criar, configurar e administrar toda a infraestrutura em nuvem por meio de arquivos de definição escritos em YAML ou JSON.  
Em vez de configurar manualmente cada recurso, como instâncias EC2, redes VPC, buckets S3 ou grupos de segurança, é possível descrever todos esses componentes de forma declarativa em um único arquivo.

Essa metodologia trata a infraestrutura como código versionável, o que facilita auditorias, manutenção e colaboração entre equipes.  
Dessa forma, o CloudFormation exemplifica o conceito de Infraestrutura como Código (IaC), proporcionando automação, consistência e agilidade na criação e gerenciamento de ambientes na AWS.

---

## Criação de uma Stack no CloudFormation

Com o CloudFormation, é possível automatizar a implantação e o controle de recursos na nuvem de maneira padronizada.  
As Stacks agrupam componentes relacionados, facilitando o gerenciamento do ciclo de vida de toda a infraestrutura e garantindo reprodutibilidade entre diferentes ambientes.

Durante meus estudos, adotei um processo estruturado para desenvolver uma Stack, validando e documentando cada etapa antes da execução.  
O fluxo seguido foi o seguinte:

### 1. Planejamento
- Identificação dos recursos necessários, como **VPCs**, **sub-redes**, **instâncias EC2**, **bancos de dados RDS**, **buckets S3** e **grupos de segurança**.  
- Análise das dependências e interações entre os componentes.

### 2. Desenvolvimento do Template
- Estruturação das seções **Parameters**, **Mappings**, **Resources**, **Outputs** e **Conditions**.  
- Garantia de que o template fosse **reutilizável**, **parametrizável** e adaptável a diferentes ambientes.

### 3. Validação
- Verificação de **sintaxe** e **lógica** utilizando o console da AWS ou ferramentas locais.  
- Correção de eventuais inconsistências antes do deploy.

### 4. Preparação e Criação da Stack
- Revisão de **parâmetros**, **tags** e **roles** de execução.  
- Processo no console ou via CLI: *upload do template → definição de parâmetros → revisão → criação da Stack.*

### 5. Acompanhamento da Execução
- Monitoramento de eventos diretamente no **CloudFormation**.  
- Consulta de logs no **CloudWatch** para confirmar o sucesso ou identificar falhas.

### 6. Atualizações e Change Sets
- Uso de **Change Sets** para revisar modificações antes da aplicação.  
- Garantia de atualizações seguras e controladas em ambientes de produção.

### 7. Rollback e Exclusão
- Compreensão do **rollback automático** em caso de falhas.  
- Execução da exclusão segura da Stack quando necessária, liberando recursos vinculados.

---

## Benefícios do uso de Stacks

O uso de Stacks centraliza o gerenciamento de recursos, permitindo criação, atualização e replicação de ambientes de forma simples e controlada.  
Além disso, as configurações podem ser versionadas em sistemas como o Git, possibilitando integração com pipelines de CI/CD.

Essa abordagem traz vantagens como:

- Padronização entre ambientes de desenvolvimento, teste e produção.  
- Governança e rastreabilidade através do versionamento do código.  
- Redução de erros manuais, aumentando a **confiabilidade** das operações na nuvem.  
- Reprodutibilidade e automação de todo o ciclo de vida da infraestrutura.

---

> O AWS CloudFormation é uma ferramenta essencial para equipes que buscam eficiência, segurança e escalabilidade na gestão de ambientes em nuvem.
