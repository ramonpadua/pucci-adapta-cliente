# STATUS — Pucci Ambiental · adapta-cliente

**Data:** 2026-10-28 · **Fase atual:** 1 (núcleo operacional do fechamento)

## Estado
- **Tasks concluídas:** 4/8 (50%). F1-T01 a F1-T04 concluídas nos limites registrados. F1-T05 segue ativa; não iniciar F1-T06 ainda.
- **F1-T05 — regra de contratos revertida e homologada:** produção na `0.0.35` (`65bbd7c`), publicada em 2026-10-20. Número de contrato obrigatório e globalmente único; `S/N` repetido e número oficial duplicado são recusados. Migração `0011_f1_t05_contracts_unique_number` aplicada; schema ativo confirma `contract_number` obrigatório e índice `idx_contracts_number`. QA (setup, estática, build, integrações) passou; `test.ran=false`. Testes sintéticos em SQLite confirmaram vazio/duplicados recusados. Em 2026-10-28, Marcela confirmou teste humano em produção: campo vazio recusado e reutilização da fixture sintética `CONTRATO-SINTETICO-001` bloqueada. Nenhum contrato real foi lido, criado, apagado ou renumerado pelo agente.
- **F1-T05 — cadastro mestre real (critério restante):** pendente confirmação da carga real dos cadastros mestres em produção (colaboradores, setores/departamentos, tomadores e CNPJs, projetos/obras e contratos), conforme política/matriz aprovadas. Não enviar dados pessoais pelo chat. Após confirmação, verificar listas e trilha antes de fechar F1-T05.
- **F1-T05 — auditoria em produção:** aceite humano das cinco coleções na trilha confirmado em 2026-10-15 (produção `0.0.29`); segue válido.
- **Produção:** `lastPublishedRef=65bbd7c` (`0.0.35`), verificado em 2026-10-28. Não iniciar F1-T06 antes de fechar F1-T05.
- **F1-T04:** B-MET-01/B-STE-01 aguardam o primeiro fechamento real medido.
- **Espelho de código no GitHub:** pendente (repositório atual é de governança; sem checkout autenticado da árvore de código).

## Ambiente
- Preview: `https://rh-pucci-3116c--preview.goskip.app` · `0.0.35` (`65bbd7c`).
- Backend: https://rh-pucci-3116c.shrd00.internal.goskip.dev
- Produção: `https://rh-pucci-3116c.goskip.app` · `lastPublishedRef=65bbd7c`.
