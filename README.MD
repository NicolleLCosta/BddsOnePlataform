# Automação OnePlatform - Configuração do projeto 

O objetivo desta documentação é orientar quanto a configuração do projeto de automação de testes da plataforma Skyone OnePlatform. 

Neste projeto, utilizamos cypress para automação dos testes e a ferramenta cucumber para escrita dos cenários e a linguagem gherkin para escrita dos BDDs.

## **Requisitos** 
  
- [Git](https://git-scm.com/) (versão 2.42.)

- [Node.js](https://nodejs.org/en/) (versão v18.18.0 LTS)  

- npm (versão 9.8.1)

### <u> Observações: </u> 

- Ao instalar o Node.js, o npm é instalado junto

- Para verificar as versões do git, Node.js e npm instaladas em seu computador, execute no seu terminal do Windows ou no git bash, o comando:

	 `git --version && node --version && npm --version`


## **Baixando o projeto**

Inicie sua IDE e selecione o diretório no qual deseja baixar o projeto, em seguida abra o terminal e execute o comando abaixo para clonar o repositório na máquina:

`git clone https://vivianesampaio@bitbucket.org/teste-bdd/bdds-oneplatform.git (exemplo)`

Os seguintes arquivos devem ter sido criados:

bdds-oneplatform/

    ├─  cypress/
        │              
        ├── .cypress-cucumber-preprocessor/  
        ├── .gitignore      
        ├── cypress.config.js
        ├── package-lockjson  
		|── package.json 

## **Configurando as dependências**

### <u> Observações: </u>

- Antes de seguir os passos abaixo, certifique-se de estar na **pasta raiz do projeto** (o mesmo diretório que o arquivo package.json/package-lock.json), caso contrário o node não irá localizar as referências necessárias para configurar o projeto.
---

Com os arquivos criados, vamos utilizar o **NPM** para configurar as dependências do projeto.

Execute o comando no terminal:

`npm install`

A pasta **`node_modules`** deve ser criada abaixo da pasta `cypress`		

## **Executando o cypress**

Com o projeto configurado, podemos executar seguinte comando no terminal para verificar se o cypress está funcionando corretamente:

`npx cypress verify`

Uma mensagem como está será exibida no terminal se a configuração estiver correta:

`✔ Verified Cypress!`

Em seguida executamos o código abaixo então a interface gráfica do cypress será mostrada na tela:

`npx cypress open`

Selecione a opção de **E2E Testing**

Em seguida, **escolha o browser onde deseja executar os teste**s e clique no botão Start E2E Testing

**Selecione a feature desejada,** então na próxima tela todos os cenários correspondentes serão testados

### <u> Observações: </u>
Por padrão, o cypress irá executar todos os cenários de testes de uma mesma feature:

Caso queira testar apenas determinados cenários você pode configurar a opção “@focus” no arquivo feature do projeto:

- Escolha a feature que deseja testar
- Abra o arquivo da feature. Digite a tag **`“@focus”`** acima do cenário que deseja testar, dessa forma, apenas os cenários sinalizados serão executados no cypress.
---
Seguindo esses passos, você será capaz de clonar o projeto de automação de testes da OnePlatform em sua máquina bem como os cenários de testes separados por funcionalidade, instalar e configurar as dependências do projeto e executar os testes automatizados da plataforma.
---
**Documentação detalhada no Confluence**
 (https://skyinone.atlassian.net/wiki/spaces/QA/pages/3682271246/WIP+Automa+o+OnePlatform+-+Configura+o+do+projeto)













