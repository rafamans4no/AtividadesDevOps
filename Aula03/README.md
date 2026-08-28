# Aula 03 — Gerência de Configuração

## O que foi estudado?

Nesta aula, o foco foi entender gerência de configuração e por que um projeto pode funcionar perfeitamente em um computador e apresentar erros em outro.

## O que é configuração?

Configuração é o conjunto de informações que determina como um sistema deve funcionar.

Entre os itens apresentados estão:

- versão da aplicação;
- versão das bibliotecas;
- banco de dados;
- portas;
- URLs;
- variáveis de ambiente;
- parâmetros de execução.


## Itens de configuração

A aula apresentou vários tipos de itens que precisam ser controlados:

### Código
Arquivos como:

```text
.js
.java
.py
```

### Dependências
Arquivos que registram bibliotecas e suas versões, como:

```text
package.json
pom.xml
```

### Configurações
Arquivos como:

```text
.env
YAML
JSON
```

### Banco de Dados
Scripts SQL e informações relacionadas ao banco.

### Infraestrutura
Tecnologias como:

```text
Docker
Terraform
```

### Documentação e scripts
Exemplos:

```text
README
build
test
deploy
```

A ideia é manter tudo isso organizado para que diferentes pessoas e ambientes consigam trabalhar de maneira consistente.

## Node.js

O Node.js é um ambiente de execução JavaScript que permite executar código no backend, ou seja, no servidor.

Para verificar se o Node.js está instalado, a aula apresentou:

```bash
node --version
```

## NPM

O **NPM (Node Package Manager)** é o gerenciador de pacotes do Node.js.

Ele facilita:

- instalação de bibliotecas;
- atualização de pacotes;
- remoção de dependências;
- gerenciamento das dependências do projeto.

Um arquivo muito importante é o:

```text
package.json
```

Ele registra as dependências do projeto.

Assim, outro desenvolvedor pode entrar no projeto e executar:

```bash
npm install
```

para instalar automaticamente os pacotes necessários.

Isso facilita bastante o trabalho em equipe e evita que cada pessoa tenha que baixar as bibliotecas manualmente.

## Criando um projeto React

A aula apresentou o comando:

```bash
npx create-react-app meu-projeto-react
```

Ele cria uma aplicação React com uma estrutura inicial pronta para desenvolvimento.

Entre os recursos criados estão:

- sistema de build;
- Babel;
- servidor local de desenvolvimento;
- scripts de build e teste;
- estrutura básica de pastas.

### Passo a passo

```bash
npx create-react-app meu-projeto-react
cd meu-projeto-react
code .
npm start
```

O último comando inicia o servidor local para visualizar o projeto no navegador.

### Arquivos principais

- **`index.js`** → ponto de entrada do React, responsável por renderizar o `App` no DOM.
- **`App.js`** → componente raiz da aplicação.
- **`App.css`** → estilos do componente `App`.
- **`index.css`** → estilos globais.


## Atividade prática

A atividade proposta foi:

1. pesquisar um template desenvolvido em React;
2. importar o projeto;
3. realizar alterações;
4. salvar em um repositório no GitHub;
5. documentar as etapas;
6. incluir prints;
7. adicionar os links do GitHub e do projeto na Vercel.

---

**Fonte:** material da Aula 03 — *Gerência de Configuração*, Prof. Me. Deivison S. Takatu.
