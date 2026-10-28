# STATUS — Pucci Ambiental · adapta-cliente

**Data:** 2026-10-28 · **Fase atual:** 1 (núcleo operacional do fechamento)

## Estado
- **Tasks concluídas:** 5/8 (62,5%). F1-T01 a F1-T05 concluídas. Próxima candidata: F1-T06 (importação de alocação e rateio) — não iniciada; aguarda pedido e autorização da Champion.
- **F1-T05 — concluída em 2026-10-28:**
  - **Regra de contratos:** produção na `0.0.35` (`65bbd7c`), publicada em 2026-10-20. Número de contrato obrigatório e globalmente único; `S/N` repetido e número oficial duplicado recusados. Migração `0011_f1_t05_contracts_unique_number` aplicada; schema ativo confirma `contract_number` obrigatório e índice `idx_contracts_number`. QA (setup, estática, build, integrações) passou; `test.ran=false`. Teste humano aprovado em 2026-10-28: campo vazio recusado e fixture sintética `CONTRATO-SINTETICO-001` bloqueada como duplicado.
  - **Cadastro mestre real:** Champion confirmou em 2026-10-28 que os cadastros reais foram lançados em produção (colaboradores, setores/departamentos, tomadores/CNPJs, projetos/obras e contratos), conforme política/matriz aprovadas. Nenhum dado pessoal passou pelo chat nem foi lido pelo agente.
  - **Trilha de auditoria:** cinco coleções confirmadas em produção em 2026-10-15 (aceite humano da Champion após “Atualizar trilha”).
  - **Integridade:** nenhum contrato real foi lido, criado, apagado ou renumerado pelo agente em todo o ciclo.
- **F1-T04:** B-MET-01/B-STE-01 aguardam o primeiro fechamento real medido.
- **Espelho de código no GitHub:** pendente (repositório atual é de governança; sem checkout autenticado da árvore de código).
- **Pedido em fila (após novo pedido da Champion):** ordenação alfabética da lista de colaboradores — análise separada, sem ler dados pessoais.

## Ambiente
- Preview: `https://rh-pucci-3116c--preview.goskip.app` · `0.0.35` (`65bbd7c`).
- Backend: https://rh-pucci-3116c.shrd00.internal.goskip.dev
- Produção: `https://rh-pucci-3116c.goskip.app` · `lastPublishedRef=65bbd7c`.
