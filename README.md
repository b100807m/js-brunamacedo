// meia-noite em paris
// como perder um homem em 10 dias
// o grande gatsby
// top gun
// 10 coisas que eu odeio em voce

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
let campoIdade;

function setup() {
  createCanvas(400, 400);
  campoIdade = createInput("15");
}

function draw() {
  background(220);
  let idade = 15; // exemplo de idade
  let recomendacao = geraRecomendacao(idade);
  text(recomendacao, width / 2, height / 2);
}

function geraRecomendacao(idade) {
  if (idade >= 10) {
    if (idade >= 14) {
      return "Meia noite em paris";
    } else {
      return "Como perder um homem em 10 dias";
    }
  } else {
    return "O grande gatsby";
  }
}
function geraRecomendacao(idade, gostaDeFantasia) {
    if(idade >= 10) {
        if(idade >= 14) {
            return "Meia-noite em paris";
        } else {
            if(gostaDeFantasia){
                return "Como perder um homem em 10 dias";
            } else {
                return "O grande gatsby";
            }
        }
    } else {
        if(gostaDeFantasia) {
            return "Top gun";
        } else {
            return "10 coisas que eu odeio em voce";
        }
    }
}
function setup() {
    createCanvas(800, 400);
    createSpan("Sua idade:");
    campoIdade = createInput("5");
    campoFantasia = createCheckbox(" Gosta de fantasia?");
}

function draw() {
    background("white");
    let idade = campoIdade.value();
    let gostaDeFantasia = campoFantasia.checked();
    let recomendacao = geraRecomendacao(idade, gostaDeFantasia);

    fill(color(76, 0, 115));
    textAlign(CENTER, CENTER);
    textSize(38);
    text(recomendacao, width / 2, height / 2);
}

function geraRecomendacao(idade, gostaDeFantasia) {
    if (idade >= 10) {
        if (idade >= 14) {
            return "Como perder um homem em 10 dias";
        } else {
            if (gostaDeFantasia) {
                return "Meia-noite em paris";
            } else {
                return "O grande gatsby";
            }
        }
    } else {
        if (gostaDeFantasia) {
            return "Top gun";
        } else {
            return "10 coisas que eu odeio em voce";
        }
    }
}
function setup() {
  createCanvas(800, 400);
  createElement("h2", "Recomendador de filmes");
  createSpan("Sua idade:");
  campoIdade = createInput("5");
  campoFantasia = createCheckbox("Gosta de fantasia?");
}
function geraRecomendacao(idade, gostaDeFantasia) {
  if (idade >= 10) {
    if (idade >= 14) {
      return "Meia-noite em paris";
    } else {
      if (idade >= 12) {
        return "O grande gatsby";
      } else {
        if (gostaDeFantasia) {
          return "Como perder um homem em 10 dias";
        } else {
          return "top gun";
        }
      }
    }
  } else {
    if (gostaDeFantasia) {
      return "meia-noite em paris";
    } else {
      return "Top gun";
    }
  }
}
function geraRecomendacao(idade, gostaDeFantasia, gostaDeAventura) {
  if (idade >= 10) {
    if (idade >= 14) {
      return "Top Gun";
    } else {
      if (idade >= 12) {
        if(gostaDeFantasia || gostaDeAventura) {
          return "10 coisas que eu odeio em voce";          
        } else{
         return "Meia-noite em paris";
        }
      } else {
        if (gostaDeFantasia) {
          return "Meia-noite em paris";
        } else {
          return "O grande gatsby";
        }
      }
    }
  } else {
    if (gostaDeFantasia) {
      return "A origem";
    } else {
      return "Como perder um homem em 10 dias";
    }
  }
}
