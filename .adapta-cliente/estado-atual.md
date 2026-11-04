# Estado atual — Adapta Cliente

- task_id: F1-T06 (importar a alocação do mês e validar o rateio de 30 dias)
- champion: Marcela
- spec: 04_fase-atual/specs/spec-1-002.md (CA-1-005, CA-1-006, CA-1-007)
- etapa: implementando (pausada)
- autorizacao_implementacao: confirmada — 2026-10-29T16:39-03:00 — “Pode implementar” (após relatório de análise e regra de rateio definida pela Champion: mesmo dia em 2 projetos = 0,50 em cada; 3 projetos = 0,33 em cada; fração exata interna, exibição a 2 casas).
- teste_humano: pendente — nada a testar ainda: migrations 0012/0013 gravadas apenas no rascunho do projeto (não aplicadas, sem QA, sem publicação); produção segue íntegra em 0.0.39 (e97fc64).
- verificacao_automatica: pendente
- aprendizado: pendente
- ultima_acao: pausa registrada pela Champion (“pare por aqui”) após a ferramenta de escrita do Skip corromper arquivos grandes de forma não determinística — migrations 0012 e 0013 reescritas e verificadas íntegras; hook /backend/v1/allocation/import parado na metade, cortado em “https://dashluisa.net”.
- proxima_acao: retomar em sessão estável — reescrever o hook de importação (prévia/confirmar, dedupe pessoa+dia+projeto, fração exata 1/N por dia, substituição atômica por competência), criar página /alocacao + serviço allocation.ts + entrada no menu, rodar QA, publicar e pedir teste humano. Nenhum dado real tocado até aqui.
- fila: [2026-11-04] botão Excluir em contratos — autorizado pela Champion para a fila (“Pode incluir na fila esta ação”); análise e autorização de implementação após o fechamento da F1-T06, com o mesmo padrão de confirmação e proteção de fixture.
- atualizado_em: 2026-11-04T16:52:00-03:00
- pendente_github: espelho da árvore de código segue pendente.
