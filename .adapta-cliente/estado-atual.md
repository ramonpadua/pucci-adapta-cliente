# Estado atual — Adapta Cliente

- task_id: F1-T05
- champion: Marcela
- spec: 04_fase-atual/specs/spec-1-002.md
- etapa: concluida
- autorizacao_implementacao: confirmada — 2026-10-20T13:47-03:00 — “Autorizo reverter a regra S/N: restaurar número de contrato obrigatório e índice global único, sem ler, apagar ou renumerar contratos reais.”
- teste_humano: aprovado — 2026-10-28T08:02-03:00 — “Testei em produção: o campo vazio foi recusado e a tentativa de reutilizar a fixture sintética CONTRATO-SINTETICO-001 foi bloqueada. Funcionou.”; carga real confirmada — 2026-10-28T09:07-03:00 — “os cadastros reais foram lançados”.
- verificacao_automatica: passou — produção `0.0.35` (`65bbd7c`): QA setup/estática/build/integrações; `test.ran=false`. SQLite sintético: vazio recusado, `S/N` duplicado recusado, número oficial duplicado recusado, número sintético único aceito. Migração `0011` aplicada; schema ativo com `contract_number` obrigatório e índice global `idx_contracts_number`. Trilha das cinco coleções validada em produção em 2026-10-15. Carga real confirmada pela Champion; nenhum registro real lido pelo agente (política de dados).
- aprendizado: capturado:06_notas/aprendizado-contínuo/AP-2026-10-28-0805-skip-qa-hook-path.md; capturado:06_notas/aprendizado-contínuo/AP-2026-10-28-0907-prova-por-metadados-de-carga.md
- ultima_acao: F1-T05 concluída — regra de contratos homologada (0.0.35) e carga real dos cadastros mestres confirmada pela Champion; fase.md, STATUS.md e changelog.md atualizados.
- proxima_acao: aguardar novo pedido da Champion para selecionar a próxima task (F1-T06 é a candidata; não iniciar sem pedido e autorização).
- atualizado_em: 2026-10-28T09:30:00-03:00
- pendente_github: espelho da árvore de código (tela, serviço, hook, migrações e schema) segue pendente; este repositório é de governança e está sincronizado.
