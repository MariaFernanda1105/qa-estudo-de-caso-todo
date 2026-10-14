# Casos de teste

**Ambiente de execução:** aplicação demonstrativa local, Chromium, Playwright. Cada caso começa em contexto de navegador isolado.

| ID | Pré-condição | Passos | Resultado esperado | Resultado observado | Status |
|---|---|---|---|---|---|
| CT-01 | Lista sem itens | Abrir a aplicação | Estado vazio visível e contador 0 | Conforme esperado | Aprovado |
| CT-02 | Lista sem itens | Informar texto válido e adicionar | Item aparece; campo limpa; contador 1 | Conforme esperado | Aprovado |
| CT-03 | Lista sem itens | Informar somente espaços e adicionar | Nenhum item criado; usuário recebe orientação clara | Item não criado; não há mensagem específica | Aprovado com observação O-01 |
| CT-04 | Uma tarefa ativa | Marcar a caixa de seleção | Item fica concluído; contador vai a 0 | Conforme esperado | Aprovado |
| CT-05 | Uma ativa e uma concluída | Abrir filtro Ativas e depois Concluídas | Cada filtro exibe apenas o estado selecionado | Conforme esperado | Aprovado |
| CT-06 | Uma tarefa cadastrada | Acionar Excluir no item | Item removido; estado vazio e contador atualizados | Conforme esperado | Aprovado |
| CT-07 | Uma tarefa cadastrada | Recarregar a página | Tarefa continua visível | Conforme esperado | Aprovado |

Captura de CT-03: `../evidencias/CT-03-entrada-em-branco.png`.

## Resultado da suíte

**7 aprovados, 0 falhas** na execução de Chromium registrada no pacote de automação. A checagem estática `npm run typecheck` também foi aprovada. O relatório HTML pode ser recriado pelo comando `npm test` no repositório Playwright.

## Rastreabilidade resumida

- RF-01: CT-01
- RF-02: CT-02
- RF-03: CT-03 (O-01)
- RF-04: CT-04
- RF-05: CT-05
- RF-06: CT-06
- RF-07: CT-07
