# Middlewares
# ToDos com middlewares 

<br>

<p align="center">
  <a href="#sobre">Sobre</a> •
  <a href="#todos">ToDos</a> •
  <a href="#instalação">Instalação</a> •
  <a href="#tecnologias">Tecnologias</a> •
  <a href="#autor">Autor</a>  
</p>

<br>

## Sobre

Projeto proposto no desafio complementar do módulo 1 da trilha do bootcamp de NodeJS da Rocketseat cujo objetivo era colocar em pratica e fixar os conceitos aprendidos sobre a construção e funcionamentos de middlewares no Node.

## ToDos

O intuito desse projeto foi construir middlewares para uma API em escrita NodeJS com o intuito de consolidar os ensinamentos do módulo I do bootcamp Ignite na trilha de NodeJS.

O projeto base da API está no meu Github, [nesse repositório](https://github.com/MrRioja/todos-ignite), e lá estão descritas as rotas e funcionalidades da aplicação. Em resumo é um projeto para gerenciamentos de to-dos.

Com base no projeto acima citado, o desafio complementar do módulo pediu a implementação dos middlewares os quais serão descritos abaixo:

### checksExistsUserAccount

Esse middleware é responsável por receber o username do usuário pelo header e validar se existe ou não um usuário com o username passado. Caso exista, o usuário é repassado para o request e a função next deve ser chamada.

### checksCreateTodosUserAvailability

Esse middleware recebe o **usuário** já dentro do request e chamar a função next apenas se esse usuário ainda estiver no **plano grátis e ainda não possuir 10 _todos_ cadastrados** ou se ele **já estiver com o plano Pro ativado**.

### checksTodoExists

Esse middleware recebe o **username** de dentro do header e o **id** de um _todo_ de dentro de `request.params`. É validado o usuário, garantido que o `id` seja um uuid e também validado que o `id` pertence a um _todo_ do usuário informado.

Com todas as validações passando, o _todo_ encontrado deve ser passado para o `request` assim como o usuário encontrado também e a função next é chamada.

### findUserById

Esse middleware possui um funcionamento semelhante ao middleware `checksExistsUserAccount` mas a busca pelo usuário é feita através do **id** de um usuário passado por parâmetro na rota. Caso o usuário tenha sido encontrado, o mesmo é repassado para dentro do `request.user` e a função next deve ser chamada.

## Instalação

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:
[Git](https://git-scm.com), [Node.js](https://nodejs.org/en/).
Além disso é bom ter um editor para trabalhar com o código como [VSCode](https://code.visualstudio.com/).

### 🎲 Rodando o Back End (servidor)

```bash
# Clone este repositório
$ git clone git@github.com:MrRioja/todos-ignite-with-middlewares.git

# Acesse a pasta do projeto no terminal/cmd
$ cd todos-ignite-with-middlewares

# Instale as dependências
$ npm install
# Caso prefira usar o Yarn execute o comando abaixo
$ yarn

# Execute a aplicação em modo de desenvolvimento
$ npm run dev
# Caso prefira usar o Yarn execute o comando abaixo
$ yarn dev

# Execute os testes da aplicação
$ npm run test
# Caso prefira usar o Yarn execute o comando abaixo
$ yarn test

# O servidor inciará na porta 3333 - acesse <http://localhost:3333>
```

## Tecnologias

<img align="left" src="https://profilinator.rishav.dev/skills-assets/nodejs-original-wordmark.svg" alt="Node.js" height="75" />

<img align="left" src="https://profilinator.rishav.dev/skills-assets/express-original-wordmark.svg" alt="Express.js" height="75"/>

<br><br><br>

## Autor

<div align="center">
<img src="https://images.weserv.nl/?url=avatars.githubusercontent.com/u/55336456?v=4&h=100&w=100&fit=cover&mask=circle&maxage=7d" />
<h1>Luiz Rioja</h1>
<strong>Backend Developer</strong>
<br/>
<br/>

<a href="https://linkedin.com/in/luizrioja" target="_blank">
<img alt="LinkedIn" src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<a href="https://github.com/mrrioja" target="_blank">
<img alt="GitHub" src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="mailto:lulyrioja@gmail.com?subject=Fala%20Dev" target="_blank">
<img alt="Gmail" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
</a>

<a href="https://api.whatsapp.com/send?phone=5511933572652" target="_blank">
<img alt="WhatsApp" src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"/>
</a>

<a href="https://join.skype.com/invite/tvBbOq03j5Uu" target="_blank">
<img alt="Skype" src="https://img.shields.io/badge/SKYPE-%2300AFF0.svg?style=for-the-badge&logo=Skype&logoColor=white"/>
</a>

<br/>
<br/>
</div>
