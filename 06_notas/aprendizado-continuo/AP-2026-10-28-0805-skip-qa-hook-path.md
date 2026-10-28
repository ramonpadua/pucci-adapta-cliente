# AP-2026-10-28-0805 — Pipeline Skip exige hook no caminho original e conferência pós-publicação

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T05 (spec-1-002) · reversão da regra S/N · Skip 0.0.33–0.0.35
- Sinal: dois comportamentos de plataforma observados no mesmo ciclo. (1) Remover o arquivo `pocketbase/hooks/contract_number_normalize.js` fez a etapa de integrações do QA falhar com "file not found on pod", mesmo com o código correto e a regra migrada para o índice do banco. (2) A publicação retornou commit `65bbd7c` (`0.0.35`) diferente do commit que passou no QA (`eb6b76d`, `0.0.34`).
- Evidência: QA run `3b474b6a` (falha de integrações) × runs `5c20aff8`/`1e8efea8` (passaram após restaurar o arquivo no mesmo caminho); `skip_project_publish` retornou `publishedRef=65bbd7c` e o status confirmou `lastPublishedRef=65bbd7c`.
- Regra reutilizável:
  - Manter o hook no caminho original que o pipeline referencia, com lógica reduzida ao necessário (exigir/aparar o campo), e deixar a regra de dados no índice/migração — não apagar o arquivo que o QA integra.
  - Não presumir que a versão validada no QA foi a publicada: conferir versão/commit ativos no Skip após publicar, antes de orientar o teste humano.
- Quando aplicar: qualquer alteração em hooks do Skip Cloud e qualquer publicação de produção no projeto.
- Quando não aplicar: não se aplica a hooks novos (criação não herda referência antiga do pipeline).
- Confiança: alta — falha e correção reproduzidas no mesmo dia, com runs e commits identificados.
- Privacidade: sem segredo, dado pessoal ou conteúdo bruto.
