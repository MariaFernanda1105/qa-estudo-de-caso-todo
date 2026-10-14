# Defeitos e observações

## O-01 — Falta de mensagem ao rejeitar tarefa composta por espaços

- **Classificação:** melhoria de usabilidade / validação de formulário.
- **Severidade:** baixa.
- **Prioridade sugerida:** média.
- **Status:** reproduzido na aplicação demonstrativa.
- **Pré-condição:** lista aberta.
- **Passos:** preencher o campo com espaços; acionar **Adicionar**.
- **Resultado atual:** a aplicação não adiciona a tarefa, mas não apresenta uma mensagem explicando a rejeição.
- **Resultado esperado:** não criar a tarefa e informar que o usuário deve inserir um texto válido, associando a mensagem ao campo.
- **Impacto:** a regra de dados é respeitada, mas o usuário pode não entender por que a ação não teve efeito.
- **Evidência:** CT-03 em `casos-de-teste.md`; reproduzível pela suíte automatizada Playwright no projeto relacionado.

Esta observação foi levantada a partir do comportamento da aplicação demonstrativa e não representa um defeito de sistema de produção. Não foram inventados outros defeitos: os demais casos da suíte passaram.
