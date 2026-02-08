# 🛡️ AI & LLM Audit Framework (SBOM + PROV-O)

Framework em Python executado no Google Colab para auditoria de proveniência e geração de SBOM (CycloneDX) em interações com modelos de IA (LLMs) utilizando o padrão PROV-O.

---

## 📖 Sobre o Projeto
Este projeto é um **estudo técnico aprofundado** desenvolvido para explorar a transparência e a rastreabilidade em sistemas de Inteligência Artificial. Ele automatiza a criação de registros de auditoria e inventários de software, permitindo documentar a origem e o ciclo de vida das respostas geradas por modelos de linguagem.

### ✨ Principais Funcionalidades
* **Geração de SBOM Dinâmico:** Criação de inventário de componentes de software via padrão **CycloneDX**.
* **Mapeamento de Proveniência:** Implementação baseada no padrão **PROV-O** (W3C) para rastrear agentes e atividades.
* **Relatório de Auditoria:** Exportação automatizada de um arquivo `relatorio_executivo.md` com formatação profissional.
* **Segurança por Design:** Execução estruturada para não exigir a exposição de chaves de API sensíveis em ambiente público.

## ⚙️ Como Utilizar
1. No topo deste repositório, clique no botão **"Open in Colab"** para abrir o notebook.
2. Execute as células em ordem sequencial (1 a 7).
3. O sistema gerará automaticamente as evidências e o relatório final para download.

## ⚠️ Notas de Implementação e Limitações
Como este é um projeto focado em segurança e aprendizado rigoroso, foram tomadas as seguintes decisões técnicas:
* **Hugging Face:** O framework opera sem a necessidade de chaves de API para evitar riscos de exposição. Por conta disso, alguns metadados avançados do modelo no SBOM podem ser limitados.
* **Ambiente:** O código foi otimizado para o Google Colab, garantindo reprodutibilidade sem necessidade de configurações locais complexas.

## 📜 Termos de Uso e Atribuição
Este código é aberto para fins de estudo e aprimoramento técnico. **Ao utilizar ou adaptar este framework, é obrigatória a citação da autoria original vinculada a este repositório:**

> **Citação sugerida:**
> *Willian. "AI & LLM Audit Framework (SBOM + PROV-O)". Disponível em: https://github.com/williamsdb/ai_llm_sbom_provo. (2026).*

---
*Este framework foi desenvolvido como um esforço técnico para fortalecer processos de **Governança, Auditoria e Segurança da Informação** em ecossistemas de IA.*
