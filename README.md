# AI LLM SBOM PROV-O

«Status: Arquivado — protótipo experimental»

Este repositório registra uma primeira tentativa experimental de investigar rastreabilidade, proveniência e inventário de componentes em aplicações que utilizam modelos de linguagem (LLMs).

O projeto foi desenvolvido no início de 2026 e representa uma etapa inicial da pesquisa que posteriormente evoluiu para abordagens mais abrangentes de rastreabilidade operacional, governança e auditoria de sistemas de IA.

Não se trata de um framework de produção nem de uma implementação de referência. O objetivo deste repositório é preservar o experimento, seus resultados e as decisões tomadas naquela etapa do desenvolvimento.

## Contexto

A questão inicial era relativamente simples:

É possível registrar a proveniência de uma interação com uma LLM e relacioná-la ao inventário de software utilizado durante sua execução?

A partir dessa questão, foi desenvolvido um protótipo em Python executado no Google Colab, combinando:

- registros de proveniência baseados em PROV-O;
- geração de SBOM utilizando CycloneDX;
- registros de auditoria em JSON;
- documentação dos resultados da execução;
- um relatório experimental consolidando as evidências produzidas.

A abordagem procurava relacionar três elementos principais:

```text
Modelo / Agente
      │
      ▼
Atividade de inferência
      │
      ▼
Resultado + contexto da execução
      │
      ├── Proveniência (PROV-O)
      └── Inventário de software (CycloneDX)
```

## O que foi experimentado

O protótipo contém um notebook que executa o fluxo experimental e produz artefatos associados à execução.

**Entre os elementos explorados estão:**

- identificação do modelo utilizado;
- registro das atividades realizadas;
- representação de entidades e agentes relacionados à execução;
- geração de inventário de componentes de software;
- registro das evidências em arquivos estruturados;
- geração de um relatório final da execução.

O repositório também preserva um registro de auditoria em JSON e uma representação visual do resultado obtido.

## Tecnologias utilizadas

- Python
- Jupyter / Google Colab
- CycloneDX
- PROV-O
- Hugging Face
- Modelos de linguagem (LLMs)

## Estrutura

```text
.
├── LICENSE
├── README.md
├── ai_llm_sbom_provo.ipynb
├── audit_log_20260208_235004.json
├── auditoria_final.png
└── relatorio_executivo.md
```

`ai_llm_sbom_provo.ipynb` contém o experimento principal.

`audit_log_20260208_235004.json` contém os registros estruturados produzidos durante uma execução.

`auditoria_final.png` apresenta uma representação visual do resultado do experimento.

`relatorio_executivo.md` reúne os resultados e observações produzidos ao final da execução.

## Limitações

Este projeto possui limitações importantes.

Ele foi desenvolvido como uma prova experimental inicial e não foi projetado para atender requisitos de produção, escalabilidade ou integração com ambientes corporativos.

Entre as principais limitações estão:

- execução dependente do Google Colab;
- forte acoplamento ao notebook;
- representação de proveniência ainda simplificada;
- cobertura limitada dos metadados relacionados ao modelo;
- ausência de uma arquitetura persistente de coleta e armazenamento de evidências;
- ausência de mecanismos abrangentes de reprodução de ambiente;
- ausência de integração entre diferentes camadas do ciclo de vida de um sistema de IA;
- validação limitada a um cenário experimental.

Consequentemente, os artefatos produzidos devem ser interpretados como evidências de uma experimentação, e não como um modelo completo de auditoria de LLMs.

## Por que este repositório permanece público

Este repositório foi mantido como registro do processo de desenvolvimento.

A abordagem utilizada aqui não foi a versão final da pesquisa. Durante seu desenvolvimento, algumas limitações ficaram evidentes, principalmente a dificuldade de representar adequadamente um sistema de IA apenas por meio da combinação entre proveniência e inventário de software.

Essa limitação levou a uma mudança de direção.

Em vez de tratar a rastreabilidade apenas como uma descrição dos componentes utilizados, o trabalho posterior passou a considerar também o que efetivamente ocorreu durante a execução: ambiente, modelo, parâmetros, recursos computacionais, telemetria, vulnerabilidades, evidências e mecanismos de integridade.

O resultado foi uma arquitetura progressivamente mais abrangente.

Portanto, este repositório deve ser entendido como um ponto de partida, e não como o resultado final dessa linha de investigação.

## Evolução

O desenvolvimento posterior seguiu esta sequência:

1. Primeiro protótipo

**AI LLM SBOM PROV-O**

Primeira tentativa experimental de relacionar proveniência de interações com LLMs e inventário de software.

Este repositório.

2. Trabalho de Conclusão de Curso

**TCC — Rastreabilidade Operacional em Modelos Fundacionais Open-Weights**

[https://github.com/williansdb/tcc_ai_governance_llms](https://github.com/williansdb/tcc_ai_governance_llms)

A investigação foi ampliada para uma arquitetura de rastreabilidade baseada em evidências, incorporando múltiplos artefatos BOM, VEX, telemetria operacional, reprodutibilidade experimental e mecanismos criptográficos de preservação das evidências.

3. BOMSenso

**BOMSenso**

[https://github.com/williansdb/bomsenso](https://github.com/williansdb/bomsenso)

A experiência acumulada foi posteriormente aplicada em uma arquitetura reprodutível voltada à segurança, rastreabilidade e governança de sistemas com IA agêntica.

```text
AI LLM SBOM PROV-O
        │
        │ primeira experimentação
        ▼
TCC — AI Governance / LLMs
        │
        │ ampliação da rastreabilidade
        ▼
BOMSenso
        │
        │ aplicação e engenharia do conceito
        ▼
Arquitetura para sistemas de IA agêntica
```

## Estado do projeto

Arquivado.

Não há previsão de desenvolvimento ativo deste protótipo.

O código permanece disponível para fins de referência, histórico técnico e acompanhamento da evolução da abordagem.

## Licença

Este projeto está disponível sob a licença MIT. Consulte o arquivo `LICENSE` para os termos completos.