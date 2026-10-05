# 📈 Assistente Pessoal de Investimentos com RPA e n8n

Este repositório é um fork do laboratório prático da **DIO**, contendo a implementação e planejamento de um pipeline automatizado no **n8n** focado em análise financeira e geração de relatórios de investimentos utilizando Inteligência Artificial (Google Gemini) e RPA.

---

## 🛠️ Arquitetura do Pipeline n8n

O workflow foi projetado utilizando nós nativos do n8n para garantir alta performance, fácil manutenção e custo zero de execução local via Docker.

- **Schedule / Manual Trigger**: Gatilho programado para rodar a análise de mercado periodicamente.
- **HTTP Request**: Coleta em tempo real das cotações e indicadores financeiros dos ativos selecionados.
- **Google Gemini Chat Model**: Processa o prompt especialista analisando os dados do mercado e gerando recomendações consolidadas.
- **Edit Fields / Set**: Sanitiza e estrutura as informações no formato Markdown/HTML para envio.
- **Gmail / Email Send**: Notifica o investidor enviando o relatório diretamente na caixa de entrada.

---

## 🧠 Prompt do Especialista em Investimentos

Atue como um analista de investimentos sênior e especialista em mercado financeiro.

Com base nos dados fornecidos:
- Preço Atual e Variação do Ativo
- Indicadores de Tendência

Faça uma análise objetiva e divida o parecer nas seguintes seções:
1. Resumo do Mercado Atual
2. Análise Técnica e Fundamentalista Rápida
3. Grau de Risco (Baixo, Médio ou Alto)
4. Recomendação de Ação (Comprar, Manter ou Aguardar)

Mantenha o tom profissional, claro e direto para tomada de decisão rápida.

---

## 🚀 Como Executar o Projeto Localmente

1. Suba a instância do n8n via Docker Desktop.
2. Acesse `http://localhost:5678` no seu navegador.
3. Importe o arquivo do fluxo.
4. Configure as credenciais do **Google Gemini API Key** e **Gmail OAuth2**.
5. Ative o fluxo!
