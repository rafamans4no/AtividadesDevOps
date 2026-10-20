# Aula 09 — Documentação de Software

## O que foi estudado?

Esta aula teve como foco a documentação de software no contexto de projetos DevOps. O objetivo principal foi compreender o que é documentar um projeto, por que isso é importante, quais tipos de documentação existem e como elaborar um README completo e útil, capaz de permitir que qualquer pessoa entenda e execute o projeto sem precisar perguntar nada para a equipe.

A documentação deve reduzir a dependência de explicações informais e permitir que outra pessoa compreenda o projeto.

---

## O que é Documentação de Software?

É o conjunto de informações que ajuda pessoas a compreender, utilizar, desenvolver, testar e manter um sistema.

Uma boa documentação responde às seguintes perguntas:

1. O que é o projeto?
2. Para que ele serve?
3. Como instalar e configurar?
4. Como executar e testar?
5. Como contribuir e realizar mudanças?

---

## Por que documentar um projeto?

A documentação apoia **quatro necessidades principais**:

| Necessidade | Descrição |
| :--- | :--- |
| **Comunicação** | Compartilhar conhecimento entre pessoas |
| **Manutenção** | Facilitar correções e evolução |
| **Colaboração** | Permitir trabalho conjunto |
| **Continuidade** | Reduzir a dependência de indivíduos |

> **Documentar não é apenas registrar, é tornar o conhecimento reutilizável.**

### O que acontece sem documentação?

* Dependência de desenvolvedores específicos;
* Dificuldade para novos integrantes entrarem no projeto;
* Configurações esquecidas ou executadas de forma diferente;
* Maior tempo para manutenção e resolução de problemas;
* Conhecimento perdido quando uma pessoa deixa a equipe;
* Perguntas repetitivas sobre instalação, execução e deploy.

### Quem utiliza a documentação?

| Perfil | Como utiliza a documentação |
| :--- | :--- |
| **Dev** | Inicia o trabalho com menor dependência da equipe |
| **Tester** | Identifica como executar e validar os testes |
| **DevOps** | Configura pipeline, ambientes e deploy |
| **Gestor** | Acompanha processos e decisões |
| **Usuário** | Aprende a utilizar o produto |

---

## Combinação de Áreas

A documentação de um projeto envolve conhecimentos de diversas áreas:

| Área | Contribuição para a documentação |
| :--- | :--- |
| **Engenharia de Software (ES)** | Requisitos, arquitetura, código e testes |
| **Gestão de Projetos (GP)** | Escopo, cronograma, riscos e entregas |
| **DevOps** | CI/CD, infraestrutura, deploy e monitoramento |
| **Segurança da Informação** | Vulnerabilidades, políticas, acessos e incidentes |
| **Qualidade de Software (QA)** | Testes, critérios de aceitação, evidências e qualidade |
| **Produto / UX** | Requisitos do usuário, jornadas, regras de negócio e usabilidade |

---

## Tipos de Documentação

| Tipo | O que descreve |
| :--- | :--- |
| **Documentação técnica** | Arquitetura, APIs, banco de dados, componentes e configurações |
| **Documentação de projeto** | Objetivos, requisitos, decisões e organização |
| **Documentação de processo** | Branches, commits, Pull Requests, testes, pipeline e deploy |

---

## GitHub — README

O **README** normalmente é o **primeiro documento consultado** em um repositório. Ele deve permitir que uma pessoa entenda rapidamente:

* Propósito do projeto;
* Principais tecnologias;
* Pré-requisitos;
* Instalação e execução;
* Testes;
* Contribuição;
* Links importantes.

### README — Tecnologias e pré-requisitos

* Informe a **stack** necessária para executar o projeto.
* **Exemplos:** linguagem e versão; framework; banco de dados; gerenciador de pacotes; Docker (quando utilizado); Git e outras ferramentas.
* Indique **versões mínimas ou recomendadas** quando isso fizer diferença.

### README — Instalação e execução

A documentação deve transformar o processo em uma **sequência reproduzível**.

**Exemplo de fluxo:**

1. Clonar o repositório;
2. Acessar a pasta;
3. Instalar dependências;
4. Configurar variáveis;
5. Executar o projeto;
6. Acessar a aplicação;
7. Executar os testes.

### README — Configuração e variáveis

Explique quais configurações são necessárias **sem expor informações sensíveis**:

* Quais variáveis existem;
* Para que cada variável serve;
* Quais são obrigatórias;
* Como criar o arquivo de configuração;
* Quais valores podem ser utilizados como exemplo.

## Documentação do Processo DevOps

| Etapa | Descrição |
| :--- | :--- |
| **Desenvolvimento** | Implementação de funcionalidades e correções no código |
| **Git** | Controle de versão e histórico das alterações |
| **Pull Request** | Solicitação de revisão e integração das mudanças |
| **Build** | Compilação ou preparação do software para execução |
| **Testes** | Validação do funcionamento e identificação de falhas |
| **Pipeline CI/CD** | Automação das etapas de integração, validação e entrega |
| **Deploy** | Publicação da aplicação em um ambiente de execução |

## O que NÃO colocar na documentação

| Item | Cuidado necessário |
| :--- | :--- |
| **Senhas e credenciais** | Nunca registrar senhas de usuários, administradores ou bancos de dados |
| **Chaves de API e tokens** | Não expor credenciais que permitam acessar serviços, sistemas ou recursos privados |
| **Dados sensíveis** | Evitar informações pessoais, dados confidenciais de clientes e informações internas restritas |
| **Arquivos de configuração sigilosos** | Não publicar arquivos `.env` ou configurações que contenham segredos |
| **Informações de infraestrutura restritas** | Não divulgar detalhes que facilitem acessos indevidos ou comprometam a segurança do sistema |

---

## Referências

* Fonte: material da **Aula 09 — Documentação de Software**, Prof. Me. Deivison S. Takatu (`deivison.takatu@fatec.sp.gov.br`).
* HUMBLE, J.; PRIKLADNICKI, R. *Entrega Contínua: Como Entregar Software de Forma Rápida e Confiável*. São Paulo: Bookman, 2013.
* MUNIZ, A. et al. *Jornada DevOps: Unindo Cultura Ágil, Lean e Tecnologia Para Entrega de Software Com Qualidade*. São Paulo: Brasport, 2019.
* SATO, D. *DevOps na prática: entrega de software confiável e automatizada*. São Paulo: Casa do Código, 2014.
* SILVA, R. *Entrega contínua em Android: Como automatizar a distribuição de apps*. São Paulo: Casa do Código, 2016.
* ARUNDEL, J.; DOMINGUS, J. *DevOps nativo de nuvem com Kubernetes*. São Paulo: Novatec, 2019.
* MORAES, G. *Caixa de Ferramentas DevOps: Um guia para construção, administração e arquitetura de sistemas modernos*. São Paulo: Casa do Código, 2015.
* PIRES, A.; MILITÃO, J. *Integração Contínua com Jenkins*. São Paulo: Casa do Código, 2019.
* VITALINO, J. F. N.; CASTRO, M. A. N. *Descomplicando o Docker*. 2. ed. São Paulo: Brasport, 2018.
* SILVERMAN, R. E. *Git: guia prático*. São Paulo: Novatec, 2019.
* KIM, G.; HUMBLE, J.; DEBOIS, P.; WILLIS, J. *Manual de DevOps: Como obter agilidade, confiabilidade e segurança em organizações tecnológicas*. São Paulo: Starlin Alta Editora, 2018.
