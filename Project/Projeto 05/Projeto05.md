# Automação de Processos com AWS Lambda e Amazon S3

Este projeto teve como foco a criação de tarefas automatizadas utilizando os serviços AWS Lambda e Amazon S3.  
O objetivo principal foi compreender como automatizar fluxos de trabalho na nuvem, aproveitando os recursos de escalabilidade, baixo custo e integração oferecidos pela AWS.

---

## O que é o Amazon S3?

O Amazon S3 (Simple Storage Service) é um serviço de armazenamento de objetos na nuvem fornecido pela AWS.  
Ele permite guardar arquivos de qualquer tipo ou tamanho, sejam imagens, relatórios, backups, vídeos ou logs de sistema.

### Principais características:

- **Alta durabilidade e disponibilidade:** os dados são replicados automaticamente em diferentes zonas de disponibilidade.  
- **Controle de acesso granular:** é possível aplicar políticas de segurança e permissões detalhadas para usuários e serviços.  
- **Integração nativa com outros serviços AWS:** o S3 pode acionar funções Lambda automaticamente quando um novo arquivo é criado, modificado ou removido.

> 💡 **Exemplo prático:** imagine um sistema que gera relatórios financeiros diariamente. Cada relatório pode ser armazenado em um bucket S3, garantindo segurança, persistência e fácil acesso para futuras análises.

---

## O que é o AWS Lambda?

O AWS Lambda é um serviço de computação sem servidor (serverless) que executa funções sob demanda em resposta a eventos, sem a necessidade de gerenciar servidores manualmente.

### Principais vantagens:

- **Execução orientada a eventos:** uma função Lambda pode ser disparada por eventos do S3, mensagens do SNS, requisições via API Gateway, entre outros.  
- **Escalabilidade automática:** a AWS gerencia automaticamente a quantidade de instâncias de execução conforme o volume de solicitações.  
- **Custo sob demanda:** você paga apenas pelo tempo que o código efetivamente executa.

> 💡 **Exemplo prático:** quando um arquivo CSV é enviado para um bucket S3, uma função Lambda pode ser acionada para processar os dados, gerar um resumo e armazenar os resultados em outro bucket ou banco de dados.

---

## Exemplo de Função Lambda (Node.js)

Abaixo, um exemplo simples de código Lambda desenvolvido em **Node.js**, que é acionado automaticamente quando um novo arquivo é adicionado a um bucket S3:

```javascript
// Importa o SDK da AWS
const AWS = require('aws-sdk');
const s3 = new AWS.S3();

// Função principal Lambda
exports.handler = async (event) => {
  // Obtém informações do evento gerado pelo S3
  const bucket = event.Records[0].s3.bucket.name;
  const key = decodeURIComponent(event.Records[0].s3.object.key.replace(/\+/g, ' '));

  console.log(`Novo arquivo detectado: ${key} no bucket: ${bucket}`);

  // Aqui você pode adicionar lógica adicional, como leitura, conversão ou processamento do arquivo
  try {
    const file = await s3.getObject({ Bucket: bucket, Key: key }).promise();
    console.log(`Arquivo lido com sucesso (${file.ContentLength} bytes).`);

    // Exemplo: processamento simples do conteúdo
    const resultado = `Processamento concluído para o arquivo: ${key}`;

    return {
      statusCode: 200,
      body: JSON.stringify({ message: resultado }),
    };
  } catch (error) {
    console.error('Erro ao processar o arquivo:', error);
    return {
      statusCode: 500,
      body: JSON.stringify({ error: 'Falha no processamento.' }),
    };
  }
};
