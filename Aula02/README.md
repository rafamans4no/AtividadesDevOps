# Aula 02 — Conceitos de Integração e Entrega Contínua de Software

## O que foi estudado?

Nesta aula, a ideia principal foi entender como fazer um software sair do computador do desenvolvedor e chegar ao usuário.

## DevOps

DevOps é uma cultura, filosofia e conjunto de práticas que integra Desenvolvimento (DEV) e Operações (OPS).

O ciclo apresentado na aula pode ser entendido como um loop:

**Plan → Code → Build → Test → Release → Deploy → Operate → Monitor**

- **Plan:** planejar o que será desenvolvido.
- **Code:** desenvolver, revisar e versionar o código.
- **Build:** transformar o código em um artefato que possa ser executado.
- **Test:** verificar automaticamente se o software está funcionando.
- **Release:** aprovar e versionar uma versão.
- **Deploy:** colocar a aplicação em um ambiente de produção.
- **Operate:** manter o sistema funcionando, disponível e escalável.
- **Monitor:** acompanhar métricas, logs e traces para perceber problemas.

## Integração Contínua (CI)

**CI — Continuous Integration** é a prática de integrar alterações de código frequentemente em um repositório compartilhado.

A cada novo commit, podem ser executados automaticamente:

- build da aplicação;
- testes automatizados;
- validação do código;
- verificação de falhas.

O objetivo é encontrar problemas cedo, em vez de descobrir tudo somente quando a aplicação já estiver em produção.

## Entrega Contínua (Continuous Delivery)

Na Entrega Contínua, o processo de preparar e disponibilizar o software é automatizado para que uma versão aprovada esteja sempre pronta para publicação.

O fluxo pode envolver:

**Build → Testes → Validação do ambiente → Release → Preparação para Deploy**

O foco é reduzir os riscos e deixar o software preparado para chegar à produção de maneira confiável.

## Deploy Contínuo (Continuous Deployment)

O Deploy Contínuo vai além da Entrega Contínua: depois que a alteração passa pelas validações do pipeline, ela pode ser publicada automaticamente em produção.

O fluxo apresentado foi:

**Build → Testes → Qualidade → Deploy → Monitoramento**

### CI x Continuous Delivery x Continuous Deployment

| Conceito | Ideia principal |
|---|---|
| **CI** | Integrar código frequentemente e validar automaticamente |
| **Continuous Delivery** | Manter o software sempre preparado para publicação |
| **Continuous Deployment** | Publicar automaticamente em produção após as validações |

## Versionamento

Versionar significa dar um identificador às diferentes versões de um software. Isso ajuda a saber o que mudou, quem mudou e quando mudou, além de permitir recuperar versões anteriores.

### Semantic Versioning (SemVer)

O padrão apresentado é:

**MAJOR.MINOR.PATCH**

Exemplo: **2.1.3**

- **MAJOR:** mudança incompatível com versões anteriores.
- **MINOR:** nova funcionalidade mantendo compatibilidade.
- **PATCH:** correção de bugs sem alteração da API.

Exemplos:
- `1.0.0` → primeira versão estável;
- `1.1.0` → nova funcionalidade compatível;
- `1.1.1` → correção de bug;
- `2.0.0` → mudança incompatível.

## Git

O Git é um sistema de controle de versão de arquivos. Ele permite registrar alterações, acompanhar o histórico do projeto e restaurar versões anteriores.

## Tags no Git

As **tags** são marcadores usados para identificar pontos específicos do histórico, principalmente versões importantes ou releases.

Existem:

- **Lightweight:** apenas um nome associado a um commit.
- **Annotated:** possui informações adicionais, como autor, data e mensagem.

Comandos apresentados:

```bash
git tag
git tag <nome-da-tag>
git push origin <nome-da-tag>
```

## Deploy

Deploy é o processo de colocar uma aplicação em um ambiente de produção para que ela fique disponível aos usuários.

Algumas etapas comuns são:

1. compilação;
2. configuração do ambiente;
3. testes finais;
4. publicação.

A aula também apresentou a Vercel como uma plataforma voltada à hospedagem e ao deploy de sites e aplicações modernas.

## Atividade

A atividade propôs criar um projeto com `index.html`, `style.css` e `script.js`, configurar o Git no VS Code, publicar o projeto no GitHub, realizar alterações e registrar novas versões utilizando commits e tags. Depois, era necessário documentar o processo e enviar pela plataforma Teams.

--

**Fonte:** material da Aula 02 — *Conceitos de Integração e Entrega Contínua de Software*, Prof. Me. Deivison S. Takatu.
