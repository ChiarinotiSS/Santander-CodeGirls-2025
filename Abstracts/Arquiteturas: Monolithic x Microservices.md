# ✨Arquiteturas: Monolithic x Microservices✨

---

## 🌸Monolithic (Monolítica)🌸
- Estrutura tradicional: UI + Business Layer + Data Access Layer integrados em um único bloco.
- Todo o sistema compartilha um único banco de dados.
- Alterações pequenas exigem deploy de toda a aplicação.
- Menos flexível para manutenção e escalabilidade.


## 🌸Microservices (Microsserviços)🌸
- A camada de front-end é separada dos serviços de back-end.
- Cada serviço pode ter seu próprio banco de dados.
- É recomendado que rodem em instâncias diferentes (isolamento).

---

### ✨Favorece:
- **Flexibilidade de manutenção:** atualizações em um serviço não afetam os outros.
- **Escalabilidade independente:** apenas os serviços mais usados podem ser escalados.
