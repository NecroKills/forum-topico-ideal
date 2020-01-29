<h1 align="center">
    <img alt="Launchbase" src="./.github/assets/logo.svg" width="400px" />
</h1>

<h2 align="center">
  Como elaborar seu tópico no Fórum
</h2>

<blockquote align="center">“Ninguém sabe tanto que não possa aprender. Ninguém sabe tão pouco que não tenha pra oferecer.”!</blockquote>

<p align="center">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%237159C1">
  </a>

  <a href="LICENSE" >
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%237159C1">
  </a>

</p>

<p align="center">
  <a href="#descrição">Descrição</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#como-reproduzir">Como reproduzir</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#código">Código</a>
  &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#markdown">Markdown</a>
  &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#não-resolvi-meu-problema">Não resolvi meu problema</a>
</p>

## Intro

*Fala Dev! Aqui vamos ver como montar bem a sua dúvida para facilitar o processo de identificação e solução do seu problema. Na maioria dos casos, as três seções exemplificadas abaixo são suficientes. Quanto mais detalhes você fornecer melhor* 💜

### Descrição

_Nessa seção você deve descrever da melhor maneira possível o erro que está acontecendo na sua aplicação. Isso abrange não só a descrição do tópico, mas também o título e as tags! Se algum erro for mostrado no terminal e/ou console do navegador, informe a mensagem do erro e pelo menos o início da stacktrace (pilha de arquivos por onde o erro "passou"). Por exemplo:_

Estou com um problema referente a aula "Foto de Perfil" no módulo GoBarber web. O seguinte erro é mostrado no meu terminal:

```
    Warning: Maximum update depth exceeded. This can happen when a component calls setState inside
    useEffect, but useEffect either doesn't have a dependency array, or one of the dependencies
    changes on every render.
    	in AvatarInput (at Profile/index.js:22)
    	in form (created by A)
    	in A (at Profile/index.js:21)
```

### Como reproduzir

_Nessa seção você deve descrever as ações que geraram o erro. O que você estava fazendo quando o erro aconteceu? Foi logo após implementar alguma funcionalidade específica no seu projeto, ou após clicar em algum botão? Descrever isso pode ajudar até a você mesmo a identificar a causa do problema! Por exemplo:_

Após a implementação do input da foto no unform, a página de Perfil para de responder e sou obrigado a fechar a aba do site.

### Código

_Nessa seção você deve fornecer todo o código possível para que as pessoas possam identificar seu problema. Evite fotos/prints da tela. As duas melhores formas de apresentar seu código são disponibilizando ele no **github** ou, caso não seja possível, apresentá-lo (completo ou trechos) no corpo da dúvida utilizando o markdown (dicas sobre como utilizá-lo nessa [seção](#markdown)). Por exemplo:_

No arquivo Profile/index.js foram adicionados o import do input de foto do usuário e o campo desse input no Unform.

```js
    import  AvatarInput  from  './AvatarInput';
    ...
      return (
        <Container>
          <Form initialData={profile} onSubmit={handleSubmit}>
            <AvatarInput name="avatar_id" />
    		...
           </Form>
           ...
        </Container>
      );
```

O arquivo referente ao componente AvatarInput pode ser visto nesse [link](https://github.com/Rocketseat/bootcamp-gostack-09/blob/master/src/pages/Profile/AvatarInput/index.js)

## Markdown

_Nessa seção você irá aprender quatro funcionalidades do markdown que vão te ajudar a formatar muito bem o seu tópico no fórum. Elas são bem simples:_

- Utilize `#` para marcar o início de uma **seção** do seu tópico (descrição, código, etc).
- Utilize `&nbsp;` para dar um **espaçamento** entre os elementos (deve estar entre duas quebras de linha)
- Utilize `[texto-do-link](seu-link)` para adicionar **links** ao corpo da sua mensagem
- Utilize \`\`\` (crases) para denotar o trecho como **code** (é preciso envolver todo o trecho escolhido com três crases no início e ao final)

_Ao marcar seu código como code, é possível utilizar o Syntax Highlighting. Para isso, basta adicionar a tag da linguagem ao final das três primeiras crases. Por exemplo, para códigos js, html e css ficaria assim:_

````
  Javascript

    ```js
    function sum(a, b) {
      const sumResult = a + b;
      console.log(`O resultado da soma é ${sumResult}`);
    }

    sum(5, 7);
    ```

  HTML

    ```html
    <div id="app">
      <h1>Rocketseat</h1>
      <ul class="tech-list">
        <li>Node.js</li>
        <li>ReactJs</li>
        <li>React Native</li>
      </ul>
    </div>
    ```

  CSS

    ```css
    @import "https://fonts.googleapis.com/css?family=Roboto:400,700&display=swap";

    * {
    margin: 0;
    padding: 0;
    border: 0;
    }

    body {
    background: #fff;
    font-family: "Roboto", sans-serif;
    padding-bottom: 20px;
    }

    .links a {
    color: white;
    font-weight: bold;
    font-size: 18px;
    line-height: 28px;
    margin: 0 15px;
    text-decoration: none;
    }

    .links a:hover {
    color: rgba(255, 255, 255, 0.5);
    transition: color 0.2s;
    }

    ```
````

_Para um exemplo mais visual do poder do markdown e de como ele pode turbinar seu tópico, dê uma olhada nesse gif:_

![demo gif](./.github/assets/example.gif)

_Obs. 1: O código utilizado nesse gif pode ser acessado [aqui](./.github/assets/example.txt)_

_Obs. 2: Para mais informações sobre o markdown e suas (muitas) funcionalidades, dê uma olhada nesse [guia](https://www.markdownguide.org/basic-syntax/)_

## Não resolvi meu problema

_Caso você informe as seções acima e mesmo assim não for possível identificar o seu problema, você pode tomar algumas medidas como:_

- Disponibilizar todo o seu projeto no github (caso ainda não o tenha feito)
- Informar as especificações da máquina que está utilizando (versões do sistema operacional, node, yarn, etc.)
- Criar um ambiente virtual que seja possível para qualquer um reproduzir o seu erro ([codesandbox](https://codesandbox.io/) e [gitpod](https://www.gitpod.io/)).

## Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Feito com :purple_heart: by [Rocketseat](https://rocketseat.com.br) :wave: [Entre na nossa comunidade!](https://discordapp.com/invite/gCRAFhc)
