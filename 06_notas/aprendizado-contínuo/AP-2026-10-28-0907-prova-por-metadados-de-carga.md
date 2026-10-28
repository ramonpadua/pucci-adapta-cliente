# AP-2026-10-28-0907 — Prova de carga real por metadados, sem ler registros

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T05 (spec-1-002) · fechamento da carga real dos cadastros mestres
- Sinal: o critério da task exige conferir cadastros reais, mas a política proíbe ler registros reais (nomes, CNPJs, dados pessoais). A prova pode vir dos logs de requisição do backend: método, caminho e status por coleção provam gravação sem expor conteúdo.
- Evidência: logs do Skip Cloud do projeto `59746` (fonte `requests`), filtrados por `/api/collections/<coleção>/records` com método POST/PATCH desde a publicação `0.0.35` (2026-10-20). Nenhum payload ou campo de registro foi lido.
- Regra reutilizável: para conferir carga real sem violar a política de dados, contar gravações por coleção nos logs de requisição (método + caminho + status), nunca ler registros; combinar com a confirmação humana da Champion. HTTP 200 em POST/PATCH indica gravação aceita; 400 indica recusa — não atribuir causa sem o texto do erro na tela.
- Quando aplicar: gates de carga de dados reais em coleções protegidas por política de privacidade.
- Quando não aplicar: não substitui a confirmação humana nem a trilha de auditoria; não serve para validar conteúdo ou qualidade dos dados.
- Confiança: alta — método validado no mesmo ciclo com logs reais do projeto.
- Privacidade: sem segredo, dado pessoal ou conteúdo bruto.
