# AP-2026-11-05-1245 — Record não tem getId() no JSVM; QA não executa rotas customizadas

**Contexto:** F1-T06 — hook `POST /backend/v1/allocation/import` crashou em produção (`TypeError: Object has no member 'getId'`, status 0) nas duas primeiras tentativas da Champion, embora o QA estivesse verde.

**Padrão:**
1. No JSVM do PocketBase (Skip Cloud), Record **não tem `getId()`** — usar `.id`. O formatter da plataforma reescreve o arquivo após a gravação; patch aplicado de memória deixou 3 ocorrências residuais que só a re-leitura integral pegou.
2. O QA da plataforma (setup, estática, build, integrações) **não executa rotas customizadas** — código de rota só é exercitado na primeira chamada real. Smoke-test mínimo obrigatório antes de liberar teste humano: POST sem credencial esperando 401 (prova que o hook carregou e a autenticação está no lugar).

**Regra derivada:** toda rota customizada nova recebe smoke test pós-publicação antes do convite ao teste humano; todo patch em arquivo JSVM é verificado por re-leitura integral (grep pela API removida), nunca por confiança no patch.
