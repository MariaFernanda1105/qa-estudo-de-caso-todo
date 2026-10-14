# Requisitos e critérios de aceite

## Contexto

Aplicação web demonstrativa de lista de tarefas. O armazenamento é local ao navegador (`localStorage`); não existe conta de usuário nem serviço de backend.

## Requisitos funcionais

| ID | Requisito | Critério de aceite |
|---|---|---|
| RF-01 | Visualizar lista vazia | Sem tarefas cadastradas, informar estado vazio e contador igual a zero. |
| RF-02 | Adicionar tarefa | Texto não vazio após remoção de espaços nas extremidades cria uma tarefa visível e limpa o campo. |
| RF-03 | Rejeitar entrada em branco | Texto vazio ou apenas espaços não cria tarefa. A interface deve explicar a validação ao usuário. |
| RF-04 | Concluir tarefa | A tarefa pode ser marcada e desmarcada; o contador reflete tarefas não concluídas. |
| RF-05 | Filtrar tarefas | Filtros Todas, Ativas e Concluídas exibem somente os estados correspondentes. |
| RF-06 | Excluir tarefa | A ação de excluir remove o item da lista e atualiza contador/estado vazio. |
| RF-07 | Persistir tarefas | Após recarregar a página na mesma origem/perfil, tarefas e estados continuam disponíveis. |

## Requisitos não funcionais

- RNF-01: Os controles principais devem ser identificáveis por rótulos ou nomes acessíveis.
- RNF-02: A lista deve permanecer utilizável em viewport móvel e desktop.
- RNF-03: A interface não deve depender de serviços externos para os fluxos cobertos.

## Fora de escopo

Autenticação, permissões, armazenamento remoto, múltiplos usuários, sincronização entre dispositivos, ordenação, edição de texto existente, acessibilidade auditada por especialista e testes de carga.
