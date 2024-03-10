<h1>Desafio sorteador de número secreto</h1>
<a href="https">Clique aqui e acesse o jogo</a>
<h2>/</h2>

<h2>🔖 Sobre</h2>
<p>Projeto utilizado nos cursos de lógica de programação.</p>

## 🚀 Tecnologias
<div>
  <img src="https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
</div>
<h2>Time</h2>

[<img loading="lazy" src="https://avatars.githubusercontent.com/u/79340989?s=400&u=fcfb57bc9a07b8ce0eeae1195e243bb1cb56f6d8&v=4" width=115><br><sub>Claudeny Avelino</sub>](https://github.com/ClaudenyAvelino)

## Adicionando a logica do jogo

function sortear(){
    let quantidade = parseInt(document.getElementById('quantidade').value);
    let de = parseInt(document.getElementById('de').value);
    let ate = parseInt(document.getElementById('ate').value);
    
    let sorteados = [];
    let numero;
    
    for (let i = 0; i < quantidade; i++) {
        numero = obterNumeroAleatorio(de, ate);
        sorteados.push(numero);
    }
    
    alert(sorteados);
}

## Exibindo os valores em forma de texto

Vamos novamente ao index.html, onde verificaremos onde está este texto. 

><label class="texto__paragrafo">Números sorteados: nenhum até agora</label>

Porém, ao invés do texto "Números sorteados: nenhum até agora", mudaremos para Números sorteados: ${sorteados}, passando a array dos números sorteados. Contudo, como estamos concatenando com outra variável, precisamos deixar toda a tag <label> </label> entre crases.

## Corrigindo o sorteio de números repetidos

Acessando novamente o arquivo app.js, dentro da função sortear(), temos o for(). Nesse for(), temos a variável numero, que recebe o obterNumeroAleatorio().
Então, sorteados é a nossa variável array, e todo array no JavaScript tem essa função chamada includes(), que devolve um booleano: true (verdadeiro) ou false (falso). O que esse while() está dizendo é: "enquanto a variável sorteados tem incluído esse numero". Enquanto for true, vamos entrar no nosso loop e pedir para ele fazer um novo sorteio. Porque, se isso der verdadeiro, é porque aquele número que sorteado já está dentro do nosso array, o que não queremos.