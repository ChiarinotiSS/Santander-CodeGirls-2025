# ✨Banco de Dados na AWS✨

---

## 🌸01. RDS (Relational Database Service)🌸
O Amazon RDS é um serviço gerenciado que facilita a criação, configuração e administração de bancos de dados relacionais na nuvem. Ele cuida de tarefas como: provisionamento, backups, atualizações, monitoramento e escalabilidade, deixando você focar nos aplicativos.

### 🫐Bancos suportados pelo RDS🫐

#### ✨Amazon Aurora
- Compatível com MySQL e PostgreSQL.
- Mais rápido e confiável (até 5x mais desempenho que MySQL).
- Combina velocidade e disponibilidade de bancos comerciais com a economia e simplicidade de bancos open source.
- Custo: cerca de 1/10 de bancos comerciais.

#### ✨Oracle
- Disponível em várias edições.
- Você pode usar sua licença própria ou pagar por hora.
- O RDS cuida de tarefas complexas (backups, patches, monitoramento, escalabilidade).

#### ✨Microsoft SQL Server
- Fácil de configurar e escalar na nuvem.
- Fornece acesso aos recursos nativos do SQL Server.
- Ferramentas e aplicativos que já funcionam no SQL Server local funcionam no RDS sem ajustes.

#### ✨MySQL
- Banco relacional open source muito usado em aplicações web.
- O RDS mantém compatibilidade total com o MySQL.
- Você pode usar as mesmas ferramentas e aplicativos que já usava localmente.

#### ✨PostgreSQL
- Banco de dados objeto-relacional open source.
- Foco em extensibilidade e padrões SQL.
- Suporta várias linguagens de programação para procedimentos armazenados (Java, Python, C/C++, PL/pgSQL etc.).

#### ✨MariaDB
- Fork (derivação) do MySQL, feito pelos criadores originais.
- Compatível com MySQL.
- Fácil de configurar, operar e escalar pelo RDS.

---

## 🌸02. DynamoDB (Banco NoSQL da AWS)🌸
- Banco de dados NoSQL totalmente gerenciado.
- Projetado para alta escalabilidade e baixa latência, independente do tamanho do aplicativo.
- Trabalha com dados não estruturados ou semiestruturados, o que dá flexibilidade no desenvolvimento.
- Ideal para aplicativos que exigem:
- Rapidez
- Escalabilidade automática
- Integração com outros serviços da AWS
- Ótima escolha para apps modernos que precisam crescer rapidamente na nuvem.

---

>🫐Colinha🫐
> RDS > bancos relacionais gerenciados (Aurora, MySQL, PostgreSQL, SQL Server, Oracle, MariaDB).
> DynamoDB > banco NoSQL, rápido, flexível e altamente escalável
