# Estado atual — Adapta Cliente

- task_id: F1-T05A (ajuste pós-carga: editar contratos e excluir projeto)
- champion: Marcela
- spec: 04_fase-atual/specs/spec-1-002.md (cadastro mestre) · pedido direto da Champion em 2026-10-28
- etapa: aguardando_autorizacao
- autorizacao_implementacao: ausente — pedido recebido (“antes de iniciar a F1-T06, preciso editar dois contratos e deletar um dos projetos cadastrados. Não tenho a opção editar e nem deletar ainda”); análise entregue, aguardando autorização em mensagem separada.
- teste_humano: pendente
- verificacao_automatica: pendente
- aprendizado: pendente
- ultima_acao: análise concluída — contratos têm apenas criar/listar (sem update na UI/serviço); projetos têm delete no serviço mas sem ação na UI; delete de projeto com contrato vinculado será recusado pelo banco (relação obrigatória, sem cascade) e precisa de mensagem clara; fixtures sintéticas devem ficar protegidas de editar/excluir.
- proxima_acao: aguardar autorização para implementar.
- atualizado_em: 2026-10-28T09:45:00-03:00
- pendente_github: espelho da árvore de código segue pendente; governança sincronizada.
