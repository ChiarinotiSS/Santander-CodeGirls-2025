# 🌸Criptografia de Dados na AWS🌸

A criptografia garante que dados não possam ser acessados por pessoas não autorizadas, tanto quando estão armazenados (repouso) quanto quando estão circulando (trânsito).

---

## ✨Criptografia em Repouso✨

Protege dados armazenados em discos, volumes ou bancos de dados.
Serviços que oferecem suporte nativo: Amazon S3, RDS, EBS.

**Funcionamento:** os dados são automaticamente criptografados antes de serem gravados e descriptografados ao serem acessados.

---

## 🫐Tipos de encriptação:🫐

 **Volumes (EBS):** criptografia de discos.
- Arquivos e soluções via parceiros/marketplace.

**Objetos (S3):**
- SSE (Server-Side Encryption).
- SSE com chaves do cliente.
- Criptografia do lado do cliente (o app criptografa antes de enviar).


**Bases de Dados:**
- MSSQL, Oracle, MySQL, PostgreSQL, Redshift.

---

## ✨Criptografia em Trânsito✨

- Protege os dados durante a transmissão entre cliente, serviço AWS, usa protocolos seguros (ex.: TLS/SSL), garante que os dados não sejam interceptados ou manipulados durante a transferência.

---

## ✨ Serviços de Gestão de Chaves:✨ 

### ✨AWS Key Management Service (KMS)✨
- Serviço central para criar e gerenciar chaves de criptografia. 
- Permite controle granular sobre quem pode usar uma chave e em que condições.
  
> 🫐Usado quando:🫐
> - Criptografamos dados em S3, EBS, DynamoDB, RDS.
> - Aplicações exigem criptografia personalizada (via SDK").

### ✨AWS Secrets Manager✨
- Armazena e protege credenciais sensíveis (senhas, tokens de API, strings de conexão).
- Permite rotação automática de credenciais.


> 🫐Usado quando:🫐
> - Precisamos evitar guardar senhas no código.
> - Queremos recuperar segredos de forma segura e auditável.

---

#### ✨Resumindo✨
- Em Repouso > dados parados (S3, RDS, EBS).
- Em Trânsito > dados em movimento (cliente ↔ AWS).
- KMS > gerenciamento de chaves de criptografia.
- Secrets Manager > gerenciamento de credenciais e segredos.

---

> ✨A boa prática na AWS é sempre usar criptografia em repouso + em trânsito, com KMS para chaves e Secrets Manager para credenciais. Assim, cobre-se todo o ciclo de segurança dos dados.✨
