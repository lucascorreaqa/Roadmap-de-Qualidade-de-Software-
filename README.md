# Roadmap de Qualidade de Software (PT-BR)

> Um guia completo e progressivo (iniciante → intermediário → avançado) para dominar Qualidade de Software: fundamentos, técnicas de teste, automação (Web, Mobile e API), performance, segurança, acessibilidade, SRE/observabilidade, dados/ML e IaC/K8s. Inclui trilhas, projetos práticos, templates e guias orientados a padrões.

[![Docs CC BY-SA 4.0](https://img.shields.io/badge/docs-CC%20BY--SA%204.0-lightgrey.svg)](LICENSES/LICENSE-docs-CC-BY-SA-4.0.md)
[![Code MIT](https://img.shields.io/badge/code-MIT-blue.svg)](LICENSES/LICENSE-code-MIT.md)
[![MD Lint](https://img.shields.io/badge/lint-markdownlint-informational.svg)](.github/workflows/markdown-lint.yml)
[![Link Check](https://img.shields.io/badge/check-links-informational.svg)](.github/workflows/link-check.yml)

---

## Sumário

- [Visão geral](#visão-geral)
- [Como usar este repositório](#como-usar-este-repositório)
- [Mapa visual (alto nível)](#mapa-visual-alto-nível)
- [Trilhas de aprendizagem](#trilhas-de-aprendizagem)
  - [Iniciante](#iniciante)
  - [Intermediário](#intermediário)
  - [Avançado](#avançado)
  - [Especializações](#especializações)
- [Projetos práticos (labs)](#projetos-práticos-labs)
- [Tópicos e guias](#tópicos-e-guias)
- [Ferramentas & exemplos](#ferramentas--exemplos)
- [Padrões e referências](#padrões-e-referências)
- [Boas práticas de automação](#boas-práticas-de-automação)
- [Métricas e qualidade de processo](#métricas-e-qualidade-de-processo)
- [Como contribuir](#como-contribuir)
- [Código de Conduta](#código-de-conduta)
- [Licenças](#licenças)
- [FAQ](#faq)
- [Roadmap do repositório](#roadmap-do-repositório)
- [Agradecimentos](#agradecimentos)

---

## Visão geral

Este repositório organiza **conteúdo em PT-BR** para quem quer aprender (ou aprofundar) **Qualidade de Software**. A proposta é combinar:

- **Trilhas por nível** (iniciante, intermediário, avançado).
- **Tópicos modulares** (fundamentos → prática).
- **Projetos práticos** (labs reprodutíveis).
- **Templates** prontos (plano de teste, roteiro exploratório, critérios de aceitação etc.).
- **Referências a padrões** (ISO 25010, ISO/IEC/IEEE 29119, OWASP, WCAG, DORA).

> Filosofia: aprender **fazendo**, ancorado em **padrões**, com **exemplos reais** e **trade-offs explícitos**.

---

## Como usar este repositório

1. **Escolha sua trilha** em `roadmaps/` (iniciante → avançado).  
2. **Leia o tópico correspondente** em `topicos/` para teoria + checklists.  
3. **Execute um lab** em `projetos/` (há instruções e requisitos em cada pasta).  
4. **Aprofunde nas especializações** (automação, performance, segurança, acessibilidade, SRE, dados/ML, IaC/K8s).  
5. **Traga dúvidas e melhorias** via *issues* e *pull requests* (veja `CONTRIBUTING.md`).

> Dica: mantenha um **caderno de oráculos** (como você decide se algo “está certo”) e registre **riscos** e **decisões**.

---

## Mapa visual (alto nível)

```mermaid
flowchart TD
A(Fundamentos) --> B(Estratégias de Teste)
A --> C(Requisitos & Oráculos)
B --> D(Design de Testes)
B --> E(Automação)
E --> E1(Unitário) --> E2(Integr./Contratos) --> E3(E2E Web/Mobile)
D --> F(Cobertura & Mutação)
A --> G(Modelos de Qualidade - ISO 25010)
B --> H(Explorat./Risco/Prior.)
E --> I(CI/CD e Ambientes)
J(Qualidade Externa) --> J1(Performance) --> J2(Segurança) --> J3(Acessibilidade) --> J4(Confiabilidade/SRE)
K(Processo & Métricas) --> K1(29119) --> K2(Métricas/DORA)
L(Especializações) --> L1(Dados/ML) --> L2(IaC/K8s)
