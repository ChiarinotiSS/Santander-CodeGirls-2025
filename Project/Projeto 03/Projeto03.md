# AWS CloudFormation

---

## O que é o AWS CloudFormation?

O AWS CloudFormation é uma ferramenta que permite definir, criar e gerenciar a infraestrutura da nuvem de forma automatizada através de arquivos escritos em YAML ou JSON. Ao invés de configurar manualmente cada recurso, como instâncias EC2, redes VPC, buckets S3 ou grupos de segurança, você consegue descrever todos esses elementos em um único arquivo.

Essa metodologia transforma a infraestrutura em código versionável, tornando-a mais fácil de auditar, manter e compartilhar entre equipes. O CloudFormation é, portanto, um exemplo prático do conceito de Infraestrutura como Código (IaC), oferecendo padronização, agilidade e consistência na criação e gestão de ambientes AWS.

---

## Criando uma Stack no CloudFormation

Com o CloudFormation, é possível automatizar a criação e gerenciamento de recursos na nuvem, garantindo controle total e padronização. A criação de uma Stack permite agrupar recursos relacionados e gerenciar seu ciclo de vida de forma organizada e replicável.

Durante meus estudos, segui um processo estruturado para criar uma Stack, documentando cada etapa e validando antes de executar qualquer deploy real. O fluxo básico incluído foi:

**01.** Planejamento
- Mapeamento dos elementos necessários, como VPCs, sub-redes, instâncias EC2, bancos de dados RDS, buckets S3 e Security Groups, considerando também as dependências entre eles.

**02.** Criação do template
- Estruturação de Parameters, Mappings, Resources, Outputs e Conditions, garantindo que o template fosse reutilizável, flexível e parametrizável.

**03.** Validação do template
- Verificação da sintaxe e lógica do arquivo usando o console da AWS ou ferramentas locais, prevenindo erros antes do deploy.

**04.** Preparação para criar a Stack
- Revisão de parâmetros, definição de tags e escolha da role de execução. No console ou via CLI, o processo envolve: upload do template > preenchimento de parâmetros > revisão > criação.

**05.** Monitoramento da criação
- Acompanhamento dos eventos no CloudFormation e análise de logs no CloudWatch para confirmar se a Stack foi criada corretamente ou para identificar possíveis falhas.

**06.** Atualizações controladas com Change Sets
- Antes de aplicar alterações em produção, os Change Sets permitem revisar modificações e reduzir riscos.

**07.** Rollback e exclusão da Stack
- Compreensão do rollback automático em caso de erros e execução de exclusão segura da Stack quando necessário.

---

## Vantagens de utilizar Stacks

Ao utilizar uma Stack, é possível centralizar a gestão de recursos, criar e atualizar ambientes de forma controlada e reproduzir facilmente configurações idênticas para desenvolvimento, teste e produção. Além disso, os templates podem ser versionados no Git, facilitando auditorias e revisões, integrados a pipelines de CI/CD, garantindo consistência entre ambientes e aplicando políticas de governança. Tudo isso reduz consideravelmente os erros manuais e aumenta a confiabilidade das operações na nuvem.
