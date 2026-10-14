# Estudo de Caso de QA — Lista de Tarefas

Documento demonstrativo de planejamento e execução de QA sobre uma aplicação simples de lista de tarefas. Foi elaborado para portfólio e não contém informação de sistemas ou empregadores reais.

## Resumo

O usuário pode criar tarefas, marcá-las como concluídas, filtrar a lista, excluir tarefas e recarregar a página preservando os dados. A aplicação de demonstração está no repositório complementar de automação Playwright; os requisitos e a matriz de testes deste estudo estão aqui para leitura independente.

## Resultado da validação

A suíte automatizada correspondente contém **7 cenários aprovados** em Chromium e a checagem TypeScript passou. Casos detalhados, riscos e a observação de usabilidade estão em `docs/`. Evidências reproduzíveis são armazenadas em `evidencias/`.

## Documentos

- `docs/requisitos.md` — requisitos e critérios de aceite.
- `docs/analise-de-riscos.md` — riscos priorizados e mitigação.
- `docs/casos-de-teste.md` — casos, resultados e rastreabilidade.
- `docs/defeitos-e-observacoes.md` — observação de usabilidade levantada durante a análise.
- `evidencias/` — capturas e registro da execução.

## Como reproduzir

No repositório da aplicação Playwright, siga o README para instalar dependências e executar `npm test`. A validação é local e não exige credenciais nem acesso a sistemas de terceiros.

## Escopo e limites

Este estudo demonstra raciocínio de QA, não uma auditoria de produção. Não cobre autenticação, sincronização entre usuários, backend, carga, compatibilidade extensa de navegadores nem recuperação de dados após limpeza do armazenamento local.
