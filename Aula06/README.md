# Aula 06 — Revisão Ferramentas e Pipelines

## O que foi estudado?

Esta aula teve caráter de revisão, retomando e consolidando os principais conceitos vistos nas aulas anteriores sobre DevOps, Pipelines de Integração Contínua e GitHub Actions.
## DevOps: O Ciclo Infinito do Desenvolvimento Moderno

- **PLAN (Planejamento):** definição do que será desenvolvido, como e quando, utilizando metodologias ágeis (ex.: Jira, Trello, Azure Boards) para organizar prioridades e alinhar expectativas entre produto, desenvolvimento e operações.
- **CODE (Codificação):** escrita, revisão e versionamento colaborativo do código-fonte, com boas práticas como código limpo, uso de IDEs, testes e documentação.
- **BUILD (Compilação):** transformação automatizada do código-fonte em um artefato executável (JAR, imagem Docker, pacote NPM, binário), passando por compilação, resolução de dependências, empacotamento, análise estática e publicação do artefato.
- **TEST (Testes):** execução automatizada de testes integrados ao pipeline de CI/CD, detectando problemas antes que cheguem ao usuário final.
- **RELEASE (Liberação):** ponto de decisão do pipeline, em que o artefato aprovado recebe uma versão semântica (ex.: v2.4.1) e passa por *quality gates* (cobertura de testes, análise de segurança, aprovação de stakeholders).
- **DEPLOY (Implantação):** publicação automatizada do software em produção, com rollback automático em caso de falha.
- **OPERATE (Operação):** manutenção da estabilidade, disponibilidade e escalabilidade da aplicação em produção, com infraestrutura gerenciada como código.
- **MONITOR (Monitoramento):** fecha o ciclo, coletando métricas, logs e traces para detectar anomalias e alimentar o próximo ciclo de planejamento com dados reais.

## Estrutura de Pipeline

Uma pipeline é uma sequência de validações automatizadas executadas durante o ciclo de entrega do software, seguindo três regras principais:

- **Build uma única vez** — o mesmo artefato é promovido entre os ambientes;
- **Mesmo deploy em todos os ambientes** — Desenvolvimento → Homologação → Produção;
- **Falhou? Para tudo** — nenhuma etapa continua após um erro.

Também foram revisadas as etapas específicas da pipeline (Build, Testes, Qualidade, Segurança, Artefatos/Package, Deploy, Release e Monitoramento), já detalhadas na Aula 05.

## Exemplo de Projeto

Foi apresentado novamente um projeto prático utilizando GitHub Actions para automatizar uma pipeline de CI/CD, em que cada etapa é executada automaticamente e uma falha interrompe o fluxo.

Link: [github.com/deivisontakatu/projeto-pipelines-devops](https://github.com/deivisontakatu/projeto-pipelines-devops)

## GitHub Actions (revisão)

O GitHub Actions é uma plataforma de automação integrada ao GitHub, que permite criar e executar workflows diretamente associados aos repositórios de código. Os workflows podem ser configurados de acordo com eventos do repositório, como push, pull request, criação de tags ou releases.

**GitHub Actions Marketplace:** catálogo de Actions, ferramentas e extensões (desenvolvidas pelo GitHub, por parceiros ou pela comunidade) que podem ser utilizadas nos workflows para build, testes, qualidade, segurança, deploy, cache, entre outras etapas.

Marketplace: [github.com/marketplace?type=actions](https://github.com/marketplace?type=actions)

## Entregas de Software e Automação

- **DevOps:** integra desenvolvimento, testes e operações por meio da automação, acelerando entregas de software com maior qualidade, estabilidade e redução de falhas.
- **Definição de Pipeline:** sequência automatizada de estágios responsável por conduzir o software desde o commit até o deploy de forma confiável (HUMBLE; PRIKLANDNICKI, 2013).
- **O papel das pipelines:** as pipelines de CI tornaram-se fundamentais no desenvolvimento moderno, automatizando validações e garantindo qualidade contínua durante todo o ciclo de entrega ("Pipelines promovem qualidade contínua ao longo de todo o processo de entrega" — SATO, 2014).
- **Gatilhos (Workflows):** iniciam automaticamente a partir de ações como push de código, pull requests, criação de releases e publicação de tags. Exemplo básico de configuração:

## Atividade da aula

A atividade proposta possui duas partes:

1. **Integrar uma pipeline ao projeto** utilizando o GitHub Actions, configurando a automação para que seja executada sempre que for realizado um novo push na branch principal (`main`).
2. **Buscar repositórios no GitHub** que contenham a integração de Pipeline e realizar uma análise de pelo menos três projetos, destacando **características**, **funcionalidades**, **gatilhos** e **histórico** de cada um.

## Referências
Fonte: material da Aula 06 — Revisão Ferramentas e Pipelines, Prof. Me. Deivison S. Takatu (deivison.takatu@fatec.sp.gov.br).
