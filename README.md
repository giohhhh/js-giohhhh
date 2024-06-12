lavra;

function setup() {
  createCanvas(400, 400);

  palavra = palavraAleatoria();
  
}

function palavraAleatoria() {
  
  let palavras = ["Caminhante", "Caminho", "Caminha"];
  
  return random(palavras);
}

function inicializaCores() {
  background("#B7F56F");
  fill("#C5B209");
  textSize(70 );
  textAlign(CENTER, CENTER);
}

function palavraParcial(minimo, maximo) {
  let quantidade = map(mouseX, minimo, maximo, 1, palavra.length);
  let parcial = palavra.substring(0, quantidade);
  return parcial;
}
