# AP-2026-11-17-1940 — Flipchart grava dia dividido numa única célula; auditoria nunca derruba operação

**Contexto:** F1-T06 — prévias reais da Champion revelaram que o Flipchart grava um dia dividido entre 2–4 projetos numa única célula de rótulo (`ambient jardinopolis ambient guatapara`; `p005 lodo ambient p118 sabesp 8ºct biossolido p124 lagoas regional p999 admin escritorio loja`). O extrator original casava só o primeiro código: dia inteiro atribuído a um projeto = erro de rateio silencioso, exatamente o cenário da regra 1/N da Champion (0,5 em 2 projetos; 0,33 em 3).

**Padrão:**
1. Fonte de dados legada pode carregar múltiplos registros numa célula só — o importador deve varrer a célula inteira por todos os identificadores conhecidos (nome, código, apelido declarado) e dividir o dia 1/N entre os distintos; pedaço desconhecido conta como share do dia (vira lacuna) e nunca infla o projeto errado. Casamento parcial (texto excedente) é listado na prévia ("Parciais"), nunca silencioso.
2. "Não funcionou" só vira diagnóstico nos logs; mensagem genérica do PocketBase ("Something went wrong") exige catch da transação devolvendo o erro real (`import_commit_failed` + detalhe técnico) — erro opaco custa um ciclo de reteste inteiro.
3. Auditoria interna é best-effort: falha de gravação de log é capturada e nunca reverte a transação de negócio. Na reimportação (primeira exclusão real), um hook de auditoria frágil derrubaria a operação inteira.
4. `skip_file_write` pode corromper a própria saída — re-leitura mental do conteúdo gravado pegou duas corrupções (hook de create e update de auditoria) antes de virarem QA falho.

**Regra derivada:** importador de fonte legada começa pela anatomia real do rótulo (amostra da Champion), não pelo formato ideal; toda transação de substituição devolve o erro real em caso de falha; hooks de auditoria nunca bloqueiam a operação que auditam.
