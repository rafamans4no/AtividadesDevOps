# Aula 07 — Integração e Entrega Contínua (CI/CD) Avançada

## O que foi estudado?

Esta aula aprofundou os conceitos fundamentais de **Integração Contínua (CI)** e **Entrega/Implantação Contínua (CD)**, explorando a criação de workflows complexos no GitHub Actions, reutilização de actions, gerenciamento de segredos e estratégias de implantação em diferentes ambientes.

## Conceitos Fundamentais: CI vs. CD

- **Continuous Integration (CI):** prática de automatizar a integração de alterações de código de múltiplos desenvolvedores em um único repositório. Envolve a execução automatizada de compilação (*build*), testes unitários/de integração e análise estática a cada *push* ou *pull request*.
- **Continuous Delivery (CD - Entrega Contínua):** extensão do CI onde o código aprovado nas etapas de teste é empacotado e preparado para implantação em produção. A liberação para o ambiente final depende de uma **aprovação manual**.
- **Continuous Deployment (CD - Implantação Contínua):** automação completa de todo o fluxo. Cada alteração que passa por todas as etapas da pipeline é implantada automaticamente em produção, **sem intervenção humana**.

## Anatomia de um Workflow no GitHub Actions

Foi detalhada a estrutura avançada dos arquivos YAML de configuração, destacando os seguintes componentes:

- **Events / Triggers (`on`):** definição fina de gatilhos (ex.: *push* restrito a branches específicas, agendamentos via *cron*, eventos de *pull request* ou gatilhos manuais via `workflow_dispatch`).
- **Jobs e Runner Environments:** execução de tarefas simultâneas ou sequenciais em ambientes isolados (`ubuntu-latest`, `windows-latest`, `macos-latest`).
- **Dependencies (`needs`):** encadeamento lógico de *jobs*, garantindo que etapas dependentes só executem caso as anteriores tenham sucesso.
- **Matrix Strategies (`strategy.matrix`):** execução paralela do mesmo job em múltiplas combinações de sistemas operacionais e versões de linguagens/runtimes (ex.: Node 18, 20 e 22).

## Boas Práticas e Segurança na Pipeline

- **Gerenciamento de Segredos (GitHub Secrets):** armazenamento seguro de credenciais, chaves API e tokens de acesso de forma criptografada, evitando exposição no código-fonte (`${{ secrets.SECRET_NAME }}`).
- **Quality Gates e Rulesets:** bloqueio de mesclagem em branches protegidas (`main`/`master`) caso as verificações da pipeline de CI falhem.
- **Uso de Action Versioning:** fixação de versões específicas de Actions do Marketplace (ex.: `@v4` ou hash SHA) para prevenir quebras imprevistas por atualizações de terceiros.

## Exemplo Prático e Atividade da Aula

A aula contou com uma demonstração prática de configuração de um workflow completo contendo etapas de testes, empacotamento Docker e publicação automatizada.

A atividade proposta envolveu:

1. **Implementar a estratégia de Matrix Build** na pipeline de um projeto para testar compatibilidade em múltiplos ambientes/versões.
2. **Configurar GitHub Secrets e Environments** para simular o fluxo de aprovação entre os ambientes de *Staging* e *Production*.

## Referências
Fonte: material da Aula 07 — Integração e Entrega Contínua (CI/CD) Avançada, Prof. Me. Deivison S. Takatu (deivison.takatu@fatec.sp.gov.br).
