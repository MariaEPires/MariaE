<!DOCTYPE html>
<html lang="en">
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.4/p5.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.4/addons/p5.sound.min.js"></script>
    <link rel="stylesheet" type="text/css" href="style.css">
    <meta charset="utf-8" />

  </head>
  <body>
    <main>
    </main>
    <script src="sketch.js"></script>
  </body>
</html>

let palavra;

function setup() { //preparar a tela
  createCanvas(400, 400); //criar canvas, tamanho 

 palavra = palavraAleatoria();

}

function palavraAleatoria() { //função palavra aleatória
let palavras = ["Amor e gelato", "Amor e azeitonas", "Tempestade de verão", "Divinos rivais"] //deixar palavras igual ao respectivos nomes dos livro
return random(palavras); //retornar o valor para onde a função for chamada

}

function inicializaCores() { //inicializar cores
 background("pink"); //fundo da cor branca
  fill ("black"); //preencher com a cor preta 
  textSize (40); //tamanho da palavra
  textAlign(CENTER, CENTER); //posição da palavra
 }

function palavraParcial(minimo, maximo) { //função 
  let quantidade = map(mouseX, minimo, maximo, 1, palavra.length); //quantidade de letras que vai utilizar
  let parcial = palavra.substring(0, quantidade); //pedaço da palavra
  return parcial; //retornar parcial
}
  
function draw() { //desenhar na tela
  inicializaCores () ; //inicializa cores
  let texto = palavraParcial(0, width); //variavél texto = palavraParcial 
  text(texto, 200, 200); //poição do texto
}
  
function livrosParaLerNasFérias (nome, gênero) //função livros para ler na férias. nome e gênero do livro
{
  
}
