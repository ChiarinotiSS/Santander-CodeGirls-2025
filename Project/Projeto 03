# AWS CloudFormation

---

## O que é?

O AWS CloudFormation é uma ferramenta que permite criar e gerenciar toda a infraestrutura de forma automatizada por meio de modelos escritos em YAML ou JSON. Em vez de configurar manualmente cada recurso na nuvem, como instâncias EC2, redes VPC, buckets S3 ou grupos de segurança, o CloudFormation permite que tudo seja descrito em um único arquivo. 

Essa abordagem transforma a infraestrutura em código versionável e reproduzível, o que facilita auditorias, manutenção e colaboração entre equipes. Assim, o CloudFormation consolida o conceito de Infraestrutura como Código (IaC), garantindo padronização, agilidade e consistência no provisionamento de ambientes AWS.

---

## Criando uma Stack com AWS CloudFormation

O AWS CloudFormation permite automatizar a criação e gerenciamento de toda a infraestrutura na nuvem por meio de código, garantindo padronização, automação e controle total sobre os recursos. Ao criar uma Stack, é possível agrupar recursos relacionados e gerenciar seu ciclo de vida de forma organizada e reproduzível.

Durante meu aprendizado, explorei o processo de criação de uma Stack, documentando e validando cada etapa antes de realizar qualquer deploy real. O fluxo básico que segui incluiu:

### 1. Planejamento
Identificação dos recursos necessários, como VPCs, sub-redes, EC2, RDS, S3 e Security Groups, além das dependências entre eles.

### 2. Criação do template (YAML/JSON)
Estruturação de Parameters, Mappings, Resources, Outputs e Conditions para que o template fosse parametrizável, reutilizável e flexível.

### 3. Validação do template
Checagem da sintaxe e lógica usando o console ou ferramentas locais, evitando erros antes do deploy.

### 4. Preparação para criação da Stack
Revisão de parâmetros, definição de tags e escolha da role de execução. O processo no console ou via CLI envolve upload do template > preenchimento de parâmetros > revisão > criação.

### 5. Monitoramento e acompanhamento
Observação de eventos de criação no CloudFormation e análise de logs no CloudWatch para confirmar sucesso ou identificar problemas.

### 6. Atualização controlada (Change Sets)
Geração de Change Sets para revisar alterações antes de aplicá-las, reduzindo riscos em ambientes de produção.

### 7. Rollback e exclusão
Entendimento do rollback automático em caso de falhas e exclusão segura da Stack quando necessário.

---

## Benefícios de uma Stack

Uma Stack permite gerenciar todos os recursos relacionados de forma centralizada, criar e atualizar ambientes de maneira controlada e reproduzir facilmente ambientes idênticos, como desenvolvimento, teste e produção. Além disso, possibilita versionar templates no Git, facilitando auditoria e revisão de mudanças, automatizar deploys integrados a pipelines de CI/CD, garantir consistência entre ambientes e aplicar políticas de governança, reduzindo significativamente erros manuais.
