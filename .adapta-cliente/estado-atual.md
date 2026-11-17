# Estado atual — Adapta Cliente

- task_id: F1-T06 (importar a alocação do mês e validar o rateio de 30 dias)
- champion: Marcela
- spec: 04-fase-atual/specs/spec-1-002.md (CA-1-005, CA-1-006, CA-1-007)
- etapa: concluida
- autorizacao_implementacao: confirmada — 2026-10-29T16:39-03:00 — “Pode implementar” (após relatório de análise e regra de rateio definida pela Champion: mesmo dia em 2 projetos = 0,50 em cada; 3 projetos = 0,33 em cada; fração exata interna, exibição a 2 casas). Autorizações adicionais durante a execução: apelidos via descrição e células combinadas (17/11).
- teste_humano: aprovado — 2026-11-17 — “funcionou” (teste 3: reimportação idempotente da competência 2026-11, após “Confirmei o resultado da prévia” do teste 2 e aprovação dos testes 1 e 2).
- verificacao_automatica: passou — QA 0.0.42–0.0.48 verde em setup, estática, build e integrações (test.ran=false); smoke test pós-publicação em toda versão (POST sem credencial → 401); confirmação da importação real provada nos logs (prévia 19:05, confirmação 19:10:58 UTC, HTTP 200). Produção em 0.0.48 (7ecf95f), publishedRef = ref homologada.
- aprendizado: capturado:AP-2026-11-05-1245-record-getid-jsvm-e-smoke-test.md; capturado:AP-2026-11-17-1940-celulas-combinadas-e-auditoria-best-effort.md
- ultima_acao: fechamento da F1-T06 — fase.md marcada concluída, changelog, STATUS (6/8, 75%), dois aprendizados e estado atualizado.
- proxima_acao: aguardar pedido da Champion — fila: botão Excluir em contratos (autorizado 04/11) e ordenação alfabética de colaboradores (pedido de 20/10); próxima task da fase é a F1-T07 (ficha mensal + NFs com retenção).
- fila: botão Excluir em contratos (autorizado para a fila em 04/11); ordenação alfabética de colaboradores (pedido de 20/10).
- atualizado_em: 2026-11-17T16:40:00-03:00
- pendente_github: espelho da árvore de código segue pendente.
