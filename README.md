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

## Trilhas de aprendizagem

> As trilhas são progressivas e mensuráveis. Cada trilha define **competências**, **módulos**, **labs**, **marcos (milestones)** e **critérios de saída**. Use-as junto dos tópicos em `topicos/` e dos labs em `projetos/`.

### Visão geral de progressão

* **Iniciante** → foco em **fundamentos**, **design de testes** e **estratégia** (pirâmide/quadrantes/risco).
* **Intermediário** → **automação** (unit/integration/E2E), **APIs & contratos**, **CI/CD**, **cobertura/mutação**.
* **Avançado** → **qualidade externa** (performance, segurança, acessibilidade), **confiabilidade/SRE**, **dados/ML** e **IaC/K8s**.
* **Especializações** → aprofundamentos práticos por domínio (ex.: Performance, Segurança, A11y, Mobile, etc.).

> Dica: trate cada trilha como um **projeto com entregáveis**. Ao final de cada módulo, produza evidências (relatórios, scripts, dashboards).

---

### Trilha **Iniciante** (4–6 semanas)

**Objetivo global**
Construir base sólida de qualidade: modelo **ISO 25010**, **verificação vs validação**, **oráculos**, **design de testes** e **priorização por risco**. Entregar um pacote de testes de caixa-preta para um sistema simples.

**Competências ao final**

* Explicar as **oito características** do ISO 25010 e identificar **trade-offs**.
* Elaborar **oráculos** e **critérios de aceitação** claros.
* Projetar testes com **partição de equivalência**, **valor de fronteira**, **tabela de decisão**, **estado** e **pairwise**.
* Conduzir **testes exploratórios** com **charters** e registrar achados.

**Módulos e conteúdos (com ponteiros de leitura)**

1. **Fundamentos de Qualidade**
   `topicos/fundamentos/qualidade-modelos.md`
   `topicos/fundamentos/verificação-vs-validação.md`
   `topicos/fundamentos/requisitos-e-oraculos.md`
2. **Estratégias de Teste**
   `topicos/fundamentos/estratégias-testes.md` (pirâmide, quadrantes, risco)
3. **Design de Testes (caixa-preta)**
   `topicos/design-de-testes/partição-equivalência.md`
   `topicos/design-de-testes/valor-de-fronteira.md`
   `topicos/design-de-testes/tabela-de-decisão.md`
   `topicos/design-de-testes/transição-de-estado.md`
   `topicos/design-de-testes/combinatorial-pairwise.md`
   `topicos/design-de-testes/metamorphic-e-property-based.md`
4. **Execução & Evidências**
   `templates/plano-de-teste.md`
   `templates/roteiro-exploratorio.md`
   `templates/criterio-de-aceitacao-gherkin.md`
   `templates/relatorio-defeito.md`

**Labs obrigatórios**

* `projetos/01-calc-valor-fronteira/`
* `projetos/03-e2e-web-playwright/` (fluxo mínimo, sem CI)
* Exercício de **tabela de decisão** (mini-regra fiscal) – criar em `projetos/extra/`

**Marcos**

* **M1**: Plano de teste + oráculos definidos.
* **M2**: Pacote de casos de teste revisado (equivalência/fronteira/decisão).
* **M3**: Execução de exploratório + relatório de achados.
* **M4**: Mini E2E funcionando localmente.

**Critérios de saída**

* Cobertura **significativa** de regras (não %, mas cenários-chave).
* Pelo menos **1 defeito** bem relatado com oráculo violado.
* Entregáveis versionados em `docs/iniciante/`.

---

### Trilha **Intermediário** (6–8 semanas)

**Objetivo global**
Automatizar testes de **unidade**, **integração** (com dependências reais), **E2E** robustos, **APIs** e **contratos**. Implantar **CI/CD** com relatórios, atacar **flakiness** e medir **cobertura** com **mutation testing**.

**Competências ao final**

* Escrever testes **unitários** e **de integração** determinísticos (Testcontainers/WireMock).
* Construir **E2E estáveis** (Playwright/Cypress) com **fixtures** e **traces**.
* Especificar e validar **contratos** (CDC/Pact) entre serviços.
* Configurar **GitHub Actions** com matriz, paralelismo e **quality gates**.
* Avaliar o suíte com **cobertura (ramo/condição/MC-DC)** e **mutantes** (PIT/Stryker).
* Diagnosticar e mitigar **flaky tests**.

**Módulos e conteúdos**

1. **Automação base**
   `topicos/automacao/unitario.md`
   `topicos/automacao/integração.md` (Testcontainers, WireMock)
2. **Web/Mobile & E2E**
   `topicos/automacao/e2e-web.md`
   `topicos/automacao/mobile.md`
3. **APIs & Contratos**
   `topicos/automacao/api-rest-graphql-grpc.md`
   `topicos/automacao/contratos.md`
4. **Cobertura & Mutação**
   `topicos/automacao/cobertura-e-mutation.md`
5. **Flakiness & Dados**
   `topicos/automacao/flakiness.md`
6. **CI/CD & Revisão**
   `topicos/processo-e-metricas/revisao-codigos-e-checklists.md`

**Labs obrigatórios**

* `projetos/02-api-contratos-pact/`
* `projetos/09-testcontainers-lab/`
* `projetos/03-e2e-web-playwright/` (fortalecido: *traces*, *network stubs*, *test ids*)
* `projetos/08-mutacao-pitest/`

**Marcos**

* **M1**: Pipeline GitHub Actions com **matriz** (SO/versões) e relatórios JUnit.
* **M2**: CDC funcional quebrando *build* ao violar contrato.
* **M3**: Suite E2E < **10 min**, estável (flakiness < **2%**).
* **M4**: Relatório de **mutação** com metas de *kill rate*.

**Critérios de saída**

* **CDC** cobrindo pelo menos **2 operações** críticas.
* **Cobertura**: declare e justifique metas por **risco** (ex.: módulo crítico com MC-DC).
* **Mutação**: *kill rate* mínimo (ex.: **>60%**) e plano para mutantes sobreviventes.
* Documentação em `docs/intermediario/`.

---

### Trilha **Avançado** (8–10 semanas)

**Objetivo global**
Elevar a **qualidade externa** e a **resiliência**: **performance** (SLIs/SLOs), **segurança** (OWASP), **acessibilidade** (WCAG 2.2), **confiabilidade/SRE** (chaos, timeouts, circuit breakers). Introdução a **dados/ML** e **IaC/Kubernetes**.

**Competências ao final**

* Planejar e executar **ensaios de carga** (load/stress/soak) com **thresholds** no k6/JMeter.
* Conduzir **DAST** básico (ZAP) e integrar **SAST/SCA** no pipeline.
* Auditar **A11y** (axe/Lighthouse) e propor correções.
* Definir **SLIs/SLOs**, **orçamento de erro** e práticas de **chaos** seguras.
* Validar **qualidade de dados** e monitorar **drift** de modelos em ML.
* Testar **IaC** (OPA/Conftest) e recursos de **K8s** (kuttl/helm tests).

**Módulos e conteúdos**

1. **Performance**
   `topicos/qualidade-externa/performance.md`
2. **Segurança**
   `topicos/qualidade-externa/segurança.md`
3. **Acessibilidade**
   `topicos/qualidade-externa/acessibilidade.md`
4. **Confiabilidade & SRE**
   `topicos/qualidade-externa/confiabilidade-resiliência.md`
5. **Dados/ML**
   `topicos/dados-ml/testes-de-dados.md`
   `topicos/dados-ml/testes-de-modelo.md`
   `topicos/dados-ml/mlops-qualidade.md`
6. **IaC & K8s**
   `topicos/iac-e-plataforma/testes-iac.md`
   `topicos/iac-e-plataforma/kubernetes-tests.md`
   `topicos/iac-e-plataforma/observabilidade.md`

**Labs obrigatórios**

* `projetos/04-performance-k6/`
* `projetos/05-seguranca-owasp-zap/`
* `projetos/06-acessibilidade-axe/`
* `projetos/extra/confiabilidade-resiliencia/` (chaos seguro em ambiente de demo)
* `projetos/extra/ml-drift-lab/`
* `projetos/extra/iac-policy-as-code/`
* `projetos/extra/k8s-kuttl/`

**Marcos**

* **M1**: Plano de performance + **SLIs/SLOs** definidos; relatórios com *thresholds*.
* **M2**: Pipeline com **segurança** (ZAP baseline + SCA) com *gates*.
* **M3**: Auditoria **WCAG 2.2** com registro de achados e correções propostas.
* **M4**: Cenário de **caos** controlado + relatório de resiliência (timeouts/retries/circuit breaker).
* **M5**: **Regras OPA** para Terraform/K8s com testes.

**Critérios de saída**

* Performance: SLOs atingidos e **gargalos** mapeados.
* Segurança: sem **alertas críticos** pendentes no baseline.
* A11y: sem **erros críticos** bloqueadores; recomendações priorizadas.
* Resiliência: evidência de **degradação graciosa** sob falha.

---

### Trilhas de **Especialização** (modulares)

Cada especialização assume **Intermediário** concluído (ou experiência equivalente). Use de forma independente, conforme sua necessidade.

#### Automação (Web & Mobile)

* **Objetivo**: dominar E2E moderno (Playwright/Cypress), padrões de seletores, *network stubs*, *test ids*, *fixtures*; mobile (Appium/Espresso/XCTest/Detox).
* **Conteúdos**: `topicos/automacao/e2e-web.md`, `topicos/automacao/mobile.md`.
* **Labs**: expandir `03-e2e-web-playwright/` + `mobile-demo/`.
* **Saída**: suíte estável com **traces** e **relatórios**; *flakiness* < 2%.

#### APIs & Contratos

* **Objetivo**: cobrir REST/GraphQL/gRPC com **contratos CDC**.
* **Conteúdos**: `topicos/automacao/api-rest-graphql-grpc.md`, `topicos/automacao/contratos.md`.
* **Labs**: `02-api-contratos-pact/`.
* **Saída**: contratos versionados; **breaking changes** bloqueiam *build*.

#### Performance

* **Objetivo**: escopo de carga, *test data*, cenários, SLIs/SLOs, *bottlenecks*.
* **Conteúdos**: `topicos/qualidade-externa/performance.md`.
* **Labs**: `04-performance-k6/`.
* **Saída**: relatório com **thresholds** e plano de otimização.

#### Segurança (AppSec)

* **Objetivo**: OWASP Top 10, DAST/SAST/SCA/SBOM, autenticação, *secrets*.
* **Conteúdos**: `topicos/qualidade-externa/segurança.md`.
* **Labs**: `05-seguranca-owasp-zap/` + SCA em CI.
* **Saída**: *gates* definidos por severidade; backlog de riscos priorizado.

#### Acessibilidade (A11y)

* **Objetivo**: WCAG 2.2, testes automatizados e manuais, *keyboard nav*, *contrast*.
* **Conteúdos**: `topicos/qualidade-externa/acessibilidade.md`.
* **Labs**: `06-acessibilidade-axe/`.
* **Saída**: relatórios axe/Lighthouse e plano de correção.

#### Observabilidade & SRE

* **Objetivo**: logs, métricas, traços, **SLIs/SLOs**, **orçamento de erro**, caos.
* **Conteúdos**: `topicos/iac-e-plataforma/observabilidade.md`, `topicos/qualidade-externa/confiabilidade-resiliência.md`.
* **Labs**: `extra/confiabilidade-resiliencia/`.
* **Saída**: painel com **SLIs**; runbook de incidentes.

#### Dados & ML

* **Objetivo**: **qualidade de dados**, **testes de modelo**, **drift** e **fairness**.
* **Conteúdos**: `topicos/dados-ml/*`.
* **Labs**: `extra/ml-drift-lab/`.
* **Saída**: validações automatizadas (schema & expectativas) + monitoramento.

#### DevOps / CI-CD

* **Objetivo**: matrizes, paralelismo, *caching*, artefatos, *gates* e relatórios.
* **Conteúdos**: `roadmaps/especializacoes/devops-ci-cd.md`.
* **Labs**: pipelines reais nos labs existentes.
* **Saída**: **tempo de feedback** otimizado; *gates* por risco.

#### IaC & Nuvem/K8s

* **Objetivo**: testes de Terraform, políticas OPA, testes K8s, *helm tests*.
* **Conteúdos**: `topicos/iac-e-plataforma/*`.
* **Labs**: `extra/iac-policy-as-code/`, `extra/k8s-kuttl/`.
* **Saída**: PR bloqueado por violação de política; testes de manifestos.

---

### Rubrica de avaliação (todas as trilhas)

* **Clareza de oráculos** (0–2) – oráculos explícitos e verificáveis.
* **Cobertura por risco** (0–2) – justificativa e equilíbrio (unit/integration/E2E).
* **Estabilidade do suíte** (0–2) – flakiness controlado; execução determinística.
* **Automação útil** (0–2) – valor por custo/tempo; manutenção.
* **Evidências e relatórios** (0–2) – métricas acionáveis; plano de ação.

Pontuação máxima: **10**. Mínimo recomendado para avanço: **7**.

---

### Entregáveis por trilha

* **Iniciante**: plano de teste, pacote de casos, relatório exploratório, mini E2E.
* **Intermediário**: suíte unit/integration, CDC funcional, E2E robusto, pipeline CI, relatório de mutação.
* **Avançado**: plano de performance + relatórios, auditoria A11y, relatório de segurança, experimento de caos, políticas OPA/K8s tests.
