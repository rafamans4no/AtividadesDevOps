# Aula 04 — Ferramentas de Integração e Entrega Contínua

## O que foi estudado?

Nesta aula, o foco foi conhecer ferramentas de CI/CD e entender como elas ajudam a automatizar o processo de desenvolvimento, testes e entrega de software.

## DevOps e o ciclo infinito

A aula reforçou o conceito de DevOps, apresentado como uma cultura, filosofia e conjunto de práticas que integra Desenvolvimento (DEV) e Operações (OPS).

O ciclo é:

**PLAN → CODE → BUILD → TEST → RELEASE → DEPLOY → OPERATE → MONITOR**

### 1. PLAN — Planejamento

É onde a equipe decide o que será feito, como e quando.

Foram citadas ferramentas como:

- Jira;
- Trello;
- Azure Boards.

### 2. CODE — Codificação

É quando as ideias do planejamento viram código.

Boas práticas destacadas:

- escrever código limpo e legível;
- utilizar IDEs;
- manter testes;
- documentar o projeto.

### 3. BUILD — Compilação e Build

O Build transforma o código em um artefato que pode ser testado e implantado.

Exemplos de artefatos:

- JAR;
- imagem Docker;
- pacote NPM;
- binário.

O processo pode envolver:

1. compilação;
2. resolução de dependências;
3. empacotamento;
4. análise estática;
5. publicação do artefato.

### 4. TEST — Testes automatizados

Os testes automatizados ajudam a encontrar problemas rapidamente, antes que eles cheguem ao usuário.

Quando os testes fazem parte do pipeline, cada build pode ser validado automaticamente.

A aula trouxe como exemplo uma plataforma de delivery executando milhares de testes a cada novo deploy, verificando funcionalidades como frete, pagamentos, notificações e pedidos.

### 5. RELEASE — Liberação

Depois que o software foi desenvolvido, compilado e testado, ele pode ser aprovado e versionado.

A aula retomou o versionamento semântico:

**MAJOR.MINOR.PATCH**

Exemplo:

```text
v2.4.1
```

### 6. DEPLOY — Implantação

É o momento de colocar o software aprovado em produção.

Com automação, uma implantação que poderia levar bastante tempo pode acontecer rapidamente e com mecanismos para reduzir riscos.

A aula apresentou um exemplo envolvendo microsserviços, Docker, Kubernetes e rollback automático quando uma verificação de saúde falha.

### 7. OPERATE — Operação

Depois que o sistema está em produção, é necessário mantê-lo:

- estável;
- disponível;
- escalável.

A aula destacou a utilização de automação e infraestrutura como código para facilitar essa gestão.

### 8. MONITOR — Monitoramento

O monitoramento fecha o ciclo e fornece informações para o próximo planejamento.


## Ferramentas de CI/CD

As ferramentas de CI/CD ajudam a:

- integrar alterações automaticamente;
- compilar aplicações;
- executar testes;
- verificar qualidade e segurança;
- gerar e armazenar artefatos;
- controlar versões e releases;
- realizar deploy;
- monitorar resultados;
- identificar falhas;
- integrar diferentes ferramentas e serviços.

O grande benefício é diminuir o trabalho manual e tornar o processo mais previsível.

## GitHub Actions

Um dos principais assuntos da aula foi o GitHub Actions.

Ele é uma plataforma de automação integrada ao GitHub que permite criar e executar workflows associados aos repositórios.

Os workflows podem ser executados a partir de eventos, como:

- `push`;
- `pull request`;
- criação de tags;
- releases.

Isso permite automatizar etapas do desenvolvimento diretamente a partir do repositório.

## O que é uma Pipeline?

Uma pipeline é uma sequência automatizada de etapas responsável por conduzir o software desde uma alteração no código até o deploy.

De forma bem simples:

```text
Código
  ↓
Build
  ↓
Testes
  ↓
Validações
  ↓
Release
  ↓
Deploy
  ↓
Monitoramento
```

Assim, o projeto passa por uma sequência organizada de verificações antes de chegar ao usuário.

## Atividade da aula

A atividade propôs analisar e comparar diferentes ferramentas utilizadas em processos de **Integração Contínua (CI)** e **Entrega/Implantação Contínua (CD)**.

O objetivo é identificar:

- características;
- funcionalidades;
- vantagens;
- limitações;
- diferenças;
- situações em que cada ferramenta pode ser mais adequada.

A atividade utiliza como base o artigo de **Manolov, Gotseva e Hinov (2025)** sobre a comparação entre Azure DevOps e GitHub.

---

**Fonte:** material da Aula 04 — *Ferramentas de Integração e Entrega Contínua*, Prof. Me. Deivison S. Takatu.
