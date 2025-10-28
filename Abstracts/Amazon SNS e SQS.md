# ✨Amazon SNS e SQS ✨

---

## 🌸Amazon SNS (Simple Notification Service)🌸
Serviço de mensagens assíncronas e notificações entre aplicações e microserviços, permite envio de push notifications, SMS, e-mails ou integração com SQS e Lambda.

### ✨Estrutura baseada em:✨
- Tópicos (Publisher > Subscriber)

**Tipos de tópicos:**
- **FIFO:** garante ordem (primeiro a entrar, primeiro a sair), limitado a 300 msgs/s.
- **Padrão:** alta flexibilidade, entrega em alta escala, mas sem garantir ordem.

---

## 🌸Amazon SQS (Simple Queue Service)🌸
Serviço de filas de mensagens para integração assíncrona entre sistemas, desacopla os componentes de um aplicativo, garantindo comunicação segura e organizada.

- **Tipos de filas:** FIFO e Padrão.

Funciona com consumidores, ao ler a mensagem, ela fica invisível temporariamente para evitar duplicidade.
Ideal para suavizar picos de tráfego e garantir processamento consistente.
