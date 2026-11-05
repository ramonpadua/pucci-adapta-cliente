# Estado atual — Adapta Cliente

- task_id: F1-T06 (importar a alocação do mês e validar o rateio de 30 dias)
- champion: Marcela
- spec: 04_fase-atual/specs/spec-1-002.md (CA-1-005, CA-1-006, CA-1-007)
- etapa: aguardando_teste_humano
- autorizacao_implementacao: confirmada — 2026-10-29T16:39-03:00 — “Pode implementar” (após relatório de análise e regra de rateio definida pela Champion: mesmo dia em 2 projetos = 0,50 em cada; 3 projetos = 0,33 em cada; fração exata interna, exibição a 2 casas).
- teste_humano: pendente
- verificacao_automatica: passou — QA 0.0.42 (cfb8752) e 0.0.43 (18982f9): setup, análise estática, build e integrações OK; test.ran=false. 0.0.40 falhou na migration 0012 (collectionId literal) e 0.0.41 na 0013 (fixture ausente) — corrigidas antes de publicar. Publicada em produção https://rh-pucci-3116c.goskip.app em 2026-11-05T12:08:49Z com publishedRef=18982f9.
- aprendizado: pendente
- ultima_acao: implementação concluída — coleção allocations (0012), fixtures 2099-01 (0013: 30 dias, 28 dias com lacuna, rateio 3-projetos), hook /backend/v1/allocation/import (prévia → confirmação → substituição atômica por transação; dedupe pessoa+dia+projeto; fração exata 1/N; conciliação por nome normalizado com não conciliados sinalizados), hooks de auditoria create/update/delete, serviço allocation.ts, página /alocacao com sinalização de 30 dias e entrada no menu.
- proxima_acao: teste humano da Champion em produção — ver sinalização na competência sintética 2099-01, importar competência real sem digitação, reimportar sem duplicar. Não iniciar outra task antes do fechamento.
- fila: botão Excluir em contratos — autorizado pela Champion para a fila (“Pode incluir na fila esta ação”, 2026-11-04); análise e autorização após o fechamento da F1-T06.
- atualizado_em: 2026-11-05T09:12:00-03:00
- pendente_github: espelho da árvore de código segue pendente.
