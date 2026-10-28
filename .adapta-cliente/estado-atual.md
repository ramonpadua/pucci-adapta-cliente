# Estado atual — Adapta Cliente

- task_id: F1-T05
- champion: Marcela
- spec: 04_fase-atual/specs/spec-1-002.md
- etapa: aguardando_teste_humano
- autorizacao_implementacao: confirmada — 2026-10-20T13:47-03:00 — “Autorizo reverter a regra S/N: restaurar número de contrato obrigatório e índice global único, sem ler, apagar ou renumerar contratos reais.”
- teste_humano: aprovado — 2026-10-28T08:02-03:00 — “Testei em produção: o campo vazio foi recusado e a tentativa de reutilizar a fixture sintética CONTRATO-SINTETICO-001 foi bloqueada. Funcionou.”
- verificacao_automatica: passou — versão Skip `0.0.34` (`eb6b76d`) QA setup/estática/build/integrações; `test.ran=false`. SQLite sintético: campo vazio recusado, `S/N` duplicado recusado, número oficial duplicado recusado, número sintético único aceito. Publicada em produção como `0.0.35` (`65bbd7c`) em 2026-10-20 14:07 local; migração `0011_f1_t05_contracts_unique_number` aplicada, schema ativo com `contract_number` obrigatório e índice global `idx_contracts_number`. Nenhum contrato real lido, criado, apagado ou renumerado pelo agente.
- aprendizado: capturado:06_notas/aprendizado-contínuo/AP-2026-10-20-0758-proteger-fixtures-na-edicao-de-tomador.md
- ultima_acao: Marcela aprovou o teste humano da reversão em produção (0.0.35).
- proxima_acao: conferir se os cadastros mestres reais foram lançados em produção e a trilha de auditoria; só então fechar F1-T05. Não iniciar F1-T06 antes do fechamento.
- atualizado_em: 2026-10-28T08:03:01-03:00
- pendente_github: espelho do código (tela, serviço, hook, migrações e schema) segue pendente; este arquivo foi atualizado para refletir o estado real do Skip.
