# Infraestrutura como Código com AWS CloudFormation

---

## Conceito

O AWS CloudFormation é um serviço da Amazon Web Services voltado para a criação e administração de ambientes em nuvem utilizando infraestrutura como código.
Com ele, toda a configuração de recursos, como instâncias EC2, VPCs, bancos de dados e funções Lambda, é descrita em arquivos YAML ou JSON, permitindo que a AWS automatize o provisionamento e o gerenciamento de forma padronizada.

---

## Automação e Padronização

O CloudFormation automatiza a criação de ambientes completos, dispensando a configuração manual no console da AWS.
Essa abordagem garante consistência, agilidade e facilidade na manutenção dos recursos, além de oferecer total controle sobre versões e alterações.

### Principais vantagens da automação:

- Uniformidade: ambientes de desenvolvimento, teste e produção são criados de forma idêntica.
- Rapidez: toda a infraestrutura é montada em minutos, sem necessidade de ajustes manuais.
- Versionamento: os templates podem ser versionados em repositórios Git.
- Escalabilidade: fácil ampliação e atualização de ambientes complexos.

---

## Stacks na Prática

No CloudFormation, uma Stack representa o grupo de recursos que são criados e gerenciados em conjunto.
Ao enviar um template, o serviço interpreta o código e provisiona automaticamente todos os elementos definidos, mantendo rastreabilidade e controle total sobre o ambiente.

### Exemplo de uso:

**01.** Criar um arquivo template.yaml descrevendo os recursos desejados (por exemplo, uma instância EC2 e um Security Group).

**02.** Enviar o template para o CloudFormation pelo console ou CLI.

**03.** O serviço cria automaticamente a infraestrutura e a organiza como uma Stack.

**04.** Atualizações ou exclusões são feitas diretamente pelo CloudFormation, de forma automatizada e segura.

---

## CloudFormation x Terraform

Embora ambos sigam o mesmo conceito de infraestrutura como código, o AWS CloudFormation e o Terraform têm algumas diferenças importantes.
O CloudFormation é exclusivo da AWS, sendo ideal para quem trabalha apenas dentro do ecossistema da Amazon, enquanto o Terraform é multicloud, podendo gerenciar recursos em provedores como AWS, Azure e Google Cloud.

Em relação à linguagem, o CloudFormation utiliza YAML ou JSON, já o Terraform usa HCL (HashiCorp Configuration Language), mais flexível e legível.
No CloudFormation, o gerenciamento de estado é feito automaticamente pela AWS, enquanto no Terraform o estado precisa ser armazenado localmente ou em repositórios remotos.

O CloudFormation oferece integração nativa e mais profunda com os serviços da AWS, e o Terraform tem boa compatibilidade, mas através de APIs externas.
Ambos são gratuitos, no CloudFormation, você paga apenas pelos recursos criados, e quanto à curva de aprendizado, o CloudFormation tende a ser mais simples para quem utiliza apenas AWS, enquanto o Terraform é mais flexível, porém exige mais configuração.

---

## O que aprendi neste desafio

Durante este desafio, compreendi como a infraestrutura como código transforma o modo de gerenciar ambientes em nuvem, tornando processos que antes eram manuais em tarefas totalmente automatizadas e reprodutíveis.
Aprendi a estruturar templates CloudFormation, criar stacks completas e entender como o controle de estado e versionamento trazem mais segurança e eficiência ao desenvolvimento.
Essa experiência fortaleceu minha base em DevOps e Cloud Computing, além de consolidar meu entendimento sobre automação e boas práticas de arquitetura em nuvem.
