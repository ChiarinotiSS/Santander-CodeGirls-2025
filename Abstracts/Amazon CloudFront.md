# ✨Amazon CloudFront✨

O Amazon CloudFront é o serviço de CDN (Content Delivery Network) da AWS, ele distribui conteúdo (imagens, vídeos, CSS, JavaScript, etc.) em pontos de presença (POPs) espalhados pelo mundo, próximos dos usuários finais.

---

## 🌸Como funciona🌸
01. O usuário faz a solicitação de um conteúdo (ex.: imagem ou vídeo).
02. O POP mais próximo entrega o conteúdo do cache.
03. O arquivo é armazenado no POP para futuras requisições.

> Caso o POP não tenha o arquivo, ele busca do servidor de origem (ex.: um bucket S3, EC2 ou servidor web).


## 🌸Benefícios🌸
- **Menor latência:** conteúdo chega mais rápido ao usuário.
- **Melhor desempenho:** páginas carregam mais rápido.
- **Menos carga no servidor de origem:** o tráfego é distribuído.
- **Escalabilidade global:** ideal para aplicações acessadas no mundo todo.
