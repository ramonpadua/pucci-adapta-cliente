# Estado atual — Adapta Cliente

- task_id: F1-T06 (importar a alocação do mês e validar o rateio de 30 dias)
- champion: Marcela
- spec: 04_fase-atual/specs/spec-1-002.md (CA-1-005, CA-1-006, CA-1-007)
- etapa: aguardando_teste_humano
- autorizacao_implementacao: confirmada — 2026-10-29T16:39-03:00 — “Pode implementar” (após relatório de análise e regra de rateio definida pela Champion: mesmo dia em 2 projetos = 0,50 em cada; 3 projetos = 0,33 em cada; fração exata interna, exibição a 2 casas).
- teste_humano: reteste pendente após correção de defeito (0.0.44)
- verificacao_automatica: passou — QA 0.0.44 (3119bc8): setup, estática, build e integrações OK; publicado em produção https://rh-pucci-3116c.goskip.app em 2026-11-05T16:44:10Z (publishedRef=3119bc8). Smoke test pós-publicação: POST /backend/v1/allocation/import sem credencial → 401 (hook carregado, recusa correta). Histórico: 0.0.42/0.0.43 (cfb8752/18982f9) QA verde mas com crash `getId` em execução que o QA não executa; 0.0.40 (0012 collectionId literal) e 0.0.41 (0013 fixture ausente) falharam no QA e foram corrigidos.
- aprendizado: AP-2026-11-05-a — Record não tem getId() no JSVM (usar .id); formatter da plataforma reescreve o arquivo e o patch inicial deixou 3 ocorrências. AP-2026-11-05-b — QA não executa rotas customizadas: smoke test mínimo é obrigatório antes de liberar teste humano.
- ultima_acao: correção do crash getId (4 pontos) + botão "Consultar competência" independente de prévia (a sinalização das fixtures 2099-01 era inalcançável no card "Rateio gravado").
- proxima_acao: reteste humano da Champion em produção — (1) fixture 2099-01: consultar competência e conferir sinalização 30/28/30; (2) importar competência real (zero digitação) e conferir rateio; (3) reimportar sem duplicar; (4) reconhecer falha em erro sem mensagem clara, tela branca ou duplicatas.
- fila: botão Excluir em contratos — autorizado pela Champion para a fila (“Pode incluir na fila esta ação”, 2026-11-04); análise e autorização após o fechamento da F1-T06.
- atualizado_em: 2026-11-05T13:47:00-03:00
- pendente_github: espelho da árvore de código segue pendente.
