# STATUS — Pucci Ambiental · adapta-cliente

**Data:** 2026-11-17 · **Fase atual:** 1 (núcleo operacional do fechamento)

## Estado
- **Tasks concluídas:** 6/8 (75%). F1-T01 a F1-T06 concluídas.
- **F1-T06 — concluída em 2026-11-17:**
  - **Produção:** `0.0.48` (`7ecf95f`), homologada pela Champion. Importação real da competência 2026-11 com zero digitação (prévia → confirmação → transação atômica, HTTP 200 provado em logs); sinalização 30/28/30 validada nas fixtures `2099-01`; reimportação idempotente aprovada após correção de defeito (auditoria best-effort + erro real da transação na resposta).
  - **Conciliação:** colaboradores 100%; projetos por nome/código do cadastro, apelidos declarados na descrição do projeto e código embutido no rótulo do Flipchart; **células combinadas** (dia dividido entre 2–4 projetos numa única célula) rateiam 1/N entre os projetos identificados, com lista "Parciais" para casamento com texto excedente. Não conciliados ficam listados e fora da gravação até conciliar — nada descartado ou atribuído por chute.
  - **Regra de rateio vigente (decisão da Champion, 30/10):** mesmo dia em 2 projetos = 0,50 em cada; 3 projetos = 0,33 cada; fração exata interna, exibição a 2 casas.
  - **Integridade:** nenhum dado pessoal passou pelo chat nem foi lido pelo agente; rateio real gravado pela Champion em produção.
- **F1-T07 (ficha mensal + NFs com retenção):** próxima candidata — aguarda pedido e autorização da Champion.
- **F1-T04:** B-MET-01/B-STE-01 aguardam o primeiro fechamento real medido.
- **Espelho de código no GitHub:** pendente (repositório atual é de governança; sem checkout autenticado da árvore de código).
- **Fila da Champion:** botão Excluir em contratos (autorizado para a fila em 04/11); ordenação alfabética da lista de colaboradores (pedido de 20/10) — análise separada, sem ler dados pessoais.

## Ambiente
- Preview: `https://rh-pucci-3116c--preview.goskip.app` · `0.0.48` (`7ecf95f`).
- Backend: https://rh-pucci-3116c.shrd00.internal.goskip.dev
- Produção: `https://rh-pucci-3116c.goskip.app` · `0.0.48` (`7ecf95f`, `lastPublishedRef=7ecf95f`).
