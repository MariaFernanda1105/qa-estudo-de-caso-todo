# Análise de riscos

Escala qualitativa: probabilidade e impacto baixos/médios/altos. A prioridade combina as duas dimensões para orientar a execução.

| ID | Risco | Probabilidade | Impacto | Prioridade | Mitigação / cobertura |
|---|---|---:|---:|---:|---|
| R-01 | Tarefa aceita com texto vazio ou apenas espaços | Média | Médio | Média | Validar campo obrigatório e regra de trim; testar valor em branco e comunicação da validação. |
| R-02 | Contador diverge da quantidade de tarefas ativas | Média | Alto | Alta | Testar inclusão, conclusão, reabertura e exclusão em estados combinados. |
| R-03 | Filtros escondem ou exibem tarefas do estado errado | Média | Médio | Média | Criar tarefas ativas e concluídas e validar os três filtros. |
| R-04 | Dados desaparecem após recarga | Baixa | Alto | Média | Recarregar a página e verificar dados e estado concluído. |
| R-05 | Ação de exclusão remove o item errado ou não o remove | Baixa | Médio | Baixa | Usar locators ligados ao nome do item; verificar remoção e atualização da lista. |
| R-06 | Controles ficam difíceis de usar com leitor de tela/teclado | Média | Alto | Alta | Priorizar labels, roles, foco visível e execução por teclado; complementar com auditoria de acessibilidade. |
| R-07 | Mudança em serviço externo impede os testes | Baixa | Médio | Baixa | Aplicação local, sem dependência de backend ou rede. |

## Priorização de execução

1. Fluxos críticos: criação, conclusão, persistência e contador (R-01, R-02, R-04).
2. Fluxos complementares: filtros e exclusão (R-03, R-05).
3. Revisão transversal: usabilidade, foco e nomes acessíveis (R-06).

## Premissas

- O navegador mantém armazenamento local entre carregamentos na mesma origem.
- A suíte automatizada roda em Chromium; outros motores e dispositivos reais ainda devem ser adicionados para ampliar a cobertura.
