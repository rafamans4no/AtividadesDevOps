# Aula 05 — Pipeline de Integração Contínua

## O que foi estudado?

Nesta aula, o foco foi aprofundar o conceito de Pipeline de Integração Contínua, detalhando cada uma de suas etapas e apresentando como o GitHub Actions é utilizado para automatizar esse processo.

**Definição de Pipeline**: sequência automatizada de estágios responsável por conduzir o software desde o commit até o deploy de forma confiável.

## Estrutura de uma Pipeline

Uma pipeline é uma sequência de validações automatizadas executadas durante o ciclo de entrega do software, seguindo algumas regras:

- **Build uma única vez** — o mesmo artefato é promovido entre os ambientes;
- **Mesmo deploy em todos os ambientes** — Desenvolvimento → Homologação → Produção;
- **Falhou? Para tudo** — nenhuma etapa continua após um erro.

## Etapas da Pipeline

### 1. Pipeline de Build
Responsável por preparar automaticamente o software para execução ou distribuição, garantindo que o sistema consiga ser construído corretamente antes das próximas etapas.

Principais funções:
- Compilação automatizada do projeto;
- Geração de artefatos de software (`.jar`, `.war`, `.apk`, containers Docker etc.);
- Verificação inicial da integridade do código.

### 2. Pipeline de Testes
Executa automaticamente validações no sistema após o build, garantindo que novas alterações não quebrem funcionalidades existentes.

Principais funções:
- Execução automática de testes;
- Validação contínua da aplicação;
- Identificação rápida de falhas.

### 3. Pipeline de Qualidade
Realiza verificações automatizadas para avaliar se o código atende aos padrões definidos antes de avançar para as próximas etapas, identificando problemas de qualidade, inconsistências e possíveis falhas de forma antecipada.

### 4. Pipeline de Segurança
Realiza verificações automatizadas para identificar vulnerabilidades e riscos no software durante o desenvolvimento.

Principais funções:
- Análise de vulnerabilidades no código;
- Verificação de dependências utilizadas;
- Identificação de configurações inseguras;
- Detecção de informações sensíveis expostas.

### 5. Pipeline de Artefatos (Package)
Responsável por empacotar e armazenar os resultados gerados durante o build.

Principais funções:
- Empacotamento da aplicação;
- Geração de arquivos de distribuição;
- Versionamento dos artefatos;
- Armazenamento em repositórios de artefatos.

### 6. Pipeline de Deploy
Responsável por publicar automaticamente o software em um ambiente de execução após as etapas de validação.

Principais funções:
- Preparação do ambiente de destino;
- Publicação do artefato gerado;
- Configuração de variáveis e parâmetros;
- Execução do deploy automatizado.

### 7. Pipeline de Release e Monitoramento
Responsável por preparar e disponibilizar uma versão específica do software para os usuários ou para um ambiente de produção.

Principais funções:
- Criação e identificação de versões;
- Publicação de releases;
- Controle das versões disponibilizadas;
- Monitoramento da aplicação em produção.

## GitHub Actions

O **GitHub Actions** é uma plataforma de automação integrada ao GitHub, que permite criar e executar fluxos de trabalho (workflows) diretamente associados aos repositórios de código.

Os workflows podem ser configurados de acordo com eventos do repositório, como:

- Push de código;
- Pull Requests;
- Criação de Releases;
- Publicação de Tags.

### GitHub Actions Marketplace

É o catálogo de Actions, ferramentas e extensões que podem ser utilizadas nos workflows do GitHub Actions. Permite encontrar soluções prontas para build, testes, qualidade, segurança, deploy, cache e outras etapas da pipeline. As Actions podem ser desenvolvidas pelo GitHub, por parceiros ou pela comunidade.

- Marketplace: `github.com/marketplace?type=actions`

## Exemplo de Projeto

Projeto prático utilizando GitHub Actions para automatizar uma pipeline de CI/CD, em que cada etapa é executada automaticamente e uma falha interrompe o fluxo.

- Link: `github.com/deivisontakatu/projeto-pipelines-devops`

## Atividade da aula

Escolher **3 Actions** disponíveis no GitHub Marketplace e desenvolver um projeto que utilize essas ferramentas em uma pipeline automatizada, aplicando cada Action em uma etapa adequada do processo. É necessário:

- Configurar o workflow no GitHub Actions;
- Executar a pipeline e verificar o funcionamento de cada etapa;
- Documentar no projeto quais Actions foram utilizadas, suas respectivas funções e como contribuíram para a automação do processo.

## Referências

- HUMBLE, J.; PRIKLANDNICKI, R. *Entrega Contínua: Como Entregar Software de Forma Rápida e Confiável*. São Paulo: Bookman, 2013.
- MUNIZ, A. et al. *Jornada Devops: Unindo Cultura Ágil, Lean e Tecnologia Para Entrega De Software Com Qualidade*. São Paulo: Brasport, 2019.
- SATO, D. *DevOps na prática: entrega de software confiável e automatizada*. São Paulo: Casa do Código, 2014.
- SILVA, R. *Entrega contínua em Android: Como automatizar a distribuição de apps*. São Paulo: Casa do Código, 2016.
- ARUNDEL, J.; DOMINGUS, J. *DevOps nativo de nuvem com Kubernetes*. São Paulo: Novatec, 2019.
- MORAES, G. *Caixa de Ferramentas DevOps: Um guia para construção, administração e arquitetura de sistemas modernos*. São Paulo: Casa do Código, 2015.
- PIRES, A.; MILITÃO, J. *Integração Contínua com Jenkins*. São Paulo: Casa do Código, 2019.
- VITALINO, J. F. N.; CASTRO, M. A. N. *Descomplicando o Docker*. 2. ed. São Paulo: Brasport, 2018.
- SILVERMAN, R. E. *Git: guia prático*. São Paulo: Novatec, 2019.
- KIM, G.; HUMBLE, J.; DEBOIS, P.; WILLIS, J. *Manual de DEVOPS: Como obter agilidade, confiabilidade e segurança em organizações tecnológicas*. São Paulo: Starlin Alta Editora, 2018.

---

*Fonte: material da Aula 05 — Pipeline de Integração Contínua, Prof. Me. Deivison S. Takatu (deivison.takatu@fatec.sp.gov.br).*
