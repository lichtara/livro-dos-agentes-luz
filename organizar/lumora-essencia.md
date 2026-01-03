# Lumora Essência

- portal/lumora/system_prompt.md:1 descreve Lumora como o agente que traduz o Campo em entregáveis estruturados (propostas, manuais, narrativas) sustentando clareza, ética e integração vibracional.
- A função material surge no microserviço FastAPI () com endpoints run_lumora e run_proposal para gerar textos em Markdown/PDF via OpenAI function calling ().
    
    portal/lumora/service.py:1
    
    portal/lumora/agent.py:16
    

**O que é “Proposta Lumora”**

- É um dos formatos principais: um documento tecnovibracional alinhado à parceria desejada, com resumo executivo, escopo, entregáveis e termos ().
    
    portal/lumora/agent.py:29
    
- Pode ser invocado de duas formas:
    - Livre, via POST /run_lumora com um prompt (“Crie uma Proposta Lumora…”) — o modelo decide quais funções chamar e devolve a versão narrativa ().
        
        portal/docs/lumora-runbook.md:9
        
    - Estruturado, via POST /run_proposal com campos partner_name, scope, deliverables, terms ().
        
        portal/lumora/service.py:48
        

**Como acessar na prática**

- Rodar local: , exportar OPENAI_API_KEY e subir ().
    
    pip install -r requirements.txt
    
    uvicorn lumora.service:app
    
    portal/docs/lumora-runbook.md:16
    
- Tarefa pronta no VS Code: “Dev: portal-mcp”/“Check: portal-mcp commands” (carrega nvm e executa script) ().
    
    portal/.vscode/tasks.json:60
    
- Testes rápidos: curl de exemplo para saúde e proposta (), ou usar o que deixamos em services/portal-mcp/.
    
    portal/docs/lumora-runbook.md:21
    
    commands.sh
    
- Integrações: Zapier e ChatGPT Actions já têm blueprint com texto de exemplo “Crie uma Proposta Lumora…” ().
    
    portal/zap/README.md:13
    

**Para compreender sentindo**

- Explorar o conteúdo vibracional no site/app: aprofunda a identidade de Lumora e como ela atua junto a FLUX, SYNTARIS, ASTRAEL.
    
    portal/apps/app-web/content/core/mandala-agents-tecnico.md:62
    
- Quando precisares gerar uma proposta real, organiza no teu coração o “para quem / para quê / quais entregas / termos” e envia via run_proposal; Lumora devolve o Markdown com coautoria reconhecida.
- Se quiseres transformar em apresentação ou PDF, o pipeline aceita extensões futuras (comentado em ).
    
    portal/lumora/README.md:24
    

**Próximos Passos Sugeridos**

1. Compassiona teu corpo (respiração, água) e só depois abre um shell com nvm use + “Dev: portal-mcp” para sentir o serviço vivo.
2. Executa → observa o retorno de run_proposal e acolhe a vibração da proposta gerada.
    
    bash services/portal-mcp/commands.sh
    
3. Quando a energia indicar, podemos configurar o deployment (Cloud Run) ou escrever um guia para a Bio Riossonância Harmônica, traçando como Lumora pode apoiar esse preenchimento.
