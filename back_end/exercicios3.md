Questão 01:
for (let i = 6; i <= 11; i++) {
  process.stdout.write(i + " ");
}

console.log("Acabou!");


Questão 02:
for (let i = 10; i >= 3; i--) {
  process.stdout.write(i + " ");
}

console.log("Acabou!");

Questão 03:
for (let i = 0; i <= 18; i += 3) {
  process.stdout.write(i + " ");
}

console.log("Acabou!");

Questão 04: 
for (let i = 100; i >= 0; i -= 5) {
  process.stdout.write(i + " ");
}

console.log("Acabou!");


Questão 05: 
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

rl.question("Digite um valor inteiro e positivo: ", (valor) => {
  const numero = parseInt(valor);

  if (isNaN(numero) || numero <= 0) {
    console.log("Por favor, digite um número inteiro positivo.");
  } else {
    process.stdout.write("Contagem: ");

    for (let i = 1; i <= numero; i++) {
      process.stdout.write(i + " ");
    }

    console.log("Acabou!");
  }

  rl.close();
});

Questão 06:
let resultado = [];

for (let i = 30; i >= 1; i--) {
  if (i % 4 === 0) {
    resultado.push(`[${i}]`);
  } else {
    resultado.push(i.toString());
  }
}

console.log(resultado.join(" "));

Questão 07:
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

let inicio, fim, incremento;

rl.question("Digite o primeiro Valor: ", (valorInicio) => {
  inicio = Number(valorInicio);

  rl.question("Digite o último Valor: ", (valorFim) => {
    fim = Number(valorFim);

    rl.question("Digite o incremento: ", (valorIncremento) => {
      incremento = Number(valorIncremento);

      let resultado = [];

      for (let i = inicio; i < fim; i += incremento) {
        resultado.push(i);
      }

      console.log("Contagem:", resultado.join(" "));
      console.log("Acabou!");

      rl.close();
    });
  });
});

Questão 08: 
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

let inicio, fim, incremento;

rl.question("Digite o primeiro Valor: ", (valorInicio) => {
  inicio = Number(valorInicio);

  rl.question("Digite o último Valor: ", (valorFim) => {
    fim = Number(valorFim);

    rl.question("Digite o incremento: ", (valorIncremento) => {
      incremento = Number(valorIncremento);

      let resultado = [];

      for (let i = inicio; i < fim; i += incremento) {
        resultado.push(i);
      }

      console.log("Contagem:", resultado.join(" "));
      console.log("Acabou!");

      rl.close();
    });
  });
});

Questão 09:
// Inicializa a variável para acumular a soma
let soma = 0;

// Loop de 6 até 100, incrementando de 2 em 2
for (let i = 6; i <= 100; i += 2) {
  soma += i;
}

// Mostra o resultado na tela
console.log("Resultado da soma:", soma);

Questão 10:
 const express = require('express');
const app = express();
const port = 3000;

// Função para calcular a soma da sequência 500 + 450 + ... + 0
function calcularSoma() {
    let soma = 0;
    for (let i = 500; i >= 0; i -= 50) {
        soma += i;
    }
    return soma;
}

// Rota principal
app.get('/', (req, res) => {
    const resultado = calcularSoma();
    res.send(`<h1>O resultado da soma é: ${resultado}</h1>`);
});

// Inicializar o servidor
app.listen(port, () => {
    console.log(`Servidor rodando em http://localhost:${port}`);
});

 
Questão 11:
 const readline = require('readline');

// Configuração da interface de leitura
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let numeros = [];
let contador = 0;

// Função para perguntar cada número
function perguntarNumero() {
    if (contador < 7) {
        rl.question(`Digite o ${contador + 1}º número inteiro: `, (resposta) => {
            const numero = parseInt(resposta, 10);

            if (isNaN(numero)) {
                console.log("Por favor, digite um número inteiro válido.");
                perguntarNumero(); // Repetir a pergunta
            } else {
                numeros.push(numero);
                contador++;
                perguntarNumero(); // Próximo número
            }
        });
    } else {
        // Todos os 7 números foram lidos
        const soma = numeros.reduce((total, num) => total + num, 0);
        console.log(`\nO somatório dos números digitados é: ${soma}`);
        rl.close();
    }
}

// Iniciar a leitura
perguntarNumero();


 Questão 12:
 const readline = require('readline');

const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let contador = 0;
let pares = 0;
let impares = 0;

function perguntarNumero() {
    if (contador < 6) {
        rl.question(`Digite o ${contador + 1}º número inteiro: `, (resposta) => {
            const numero = parseInt(resposta, 10);

            if (isNaN(numero)) {
                console.log("Por favor, digite um número inteiro válido.");
                perguntarNumero(); // Repete a pergunta
            } else {
                if (numero % 2 === 0) {
                    pares++;
                } else {
                    impares++;
                }
                contador++;
                perguntarNumero(); // Próximo número
            }
        });
    } else {
        // Todos os 6 números foram lidos
        console.log(`\nQuantidade de números pares: ${pares}`);
        console.log(`Quantidade de números ímpares: ${impares}`);
        rl.close();
    }
}

// Iniciar a leitura
perguntarNumero();


Questão 13: 
// Função para gerar um número aleatório entre 0 e 10 (inclusive)
function numeroAleatorio() {
    return Math.floor(Math.random() * 11); // 0 a 10
}

// Array para armazenar os números sorteados
let numerosSorteados = [];

// Sorteio de 20 números
for (let i = 0; i < 20; i++) {
    numerosSorteados.push(numeroAleatorio());
}

// a) Mostrar os números sorteados
console.log("Números sorteados:", numerosSorteados.join(", "));

// b) Quantos números estão acima de 5
let acimaDeCinco = numerosSorteados.filter(num => num > 5).length;
console.log("Quantidade de números acima de 5:", acimaDeCinco);

// c) Quantos números são divisíveis por 3
let divisiveisPor3 = numerosSorteados.filter(num => num % 3 === 0).length;
console.log("Quantidade de números divisíveis por 3:", divisiveisPor3);


Questão 14: 
const readline = require('readline');

const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let precos = [];
let contador = 0;

function perguntarPreco() {
    if (contador < 8) {
        rl.question(`Digite o preço do ${contador + 1}º produto: `, (resposta) => {
            const preco = parseFloat(resposta.replace(',', '.')); // Aceita vírgula ou ponto

            if (isNaN(preco) || preco < 0) {
                console.log("Por favor, digite um preço válido (número positivo).");
                perguntarPreco(); // Repetir a pergunta
            } else {
                precos.push(preco);
                contador++;
                perguntarPreco(); // Próximo preço
            }
        });
    } else {
        // Todos os preços foram lidos
        const maiorPreco = Math.max(...precos);
        const menorPreco = Math.min(...precos);

        console.log(`\nO maior preço digitado foi: R$ ${maiorPreco.toFixed(2)}`);
        console.log(`O menor preço digitado foi: R$ ${menorPreco.toFixed(2)}`);
        rl.close();
    }
}

// Iniciar a leitura
perguntarPreco();


Questão 15: 
const readline = require('readline');

const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let idades = [];
let contador = 0;

function perguntarIdade() {
    if (contador < 10) {
        rl.question(`Digite a idade da ${contador + 1}ª pessoa: `, (resposta) => {
            const idade = parseInt(resposta, 10);

            if (isNaN(idade) || idade < 0) {
                console.log("Por favor, digite uma idade válida (número inteiro não negativo).");
                perguntarIdade(); // Repetir a pergunta
            } else {
                idades.push(idade);
                contador++;
                perguntarIdade(); // Próxima idade
            }
        });
    } else {
        // Todos os 10 números foram lidos
        const soma = idades.reduce((total, i) => total + i, 0);
        const media = soma / idades.length;
        const maioresQue18 = idades.filter(i => i > 18).length;
        const menoresQue5 = idades.filter(i => i < 5).length;
        const maiorIdade = Math.max(...idades);

        console.log(`\nMédia de idade do grupo: ${media.toFixed(2)}`);
        console.log(`Quantidade de pessoas com mais de 18 anos: ${maioresQue18}`);
        console.log(`Quantidade de pessoas com menos de 5 anos: ${menoresQue5}`);
        console.log(`Maior idade lida: ${maiorIdade}`);

        rl.close();
    }
}

// Iniciar a leitura
perguntarIdade();

Questão 16:
const readline = require('readline');

// Função para ler entrada do usuário usando promise
function perguntar(pergunta) {
    const rl = readline.createInterface({
        input: process.stdin,
        output: process.stdout
    });

    return new Promise(resolve => {
        rl.question(pergunta, resposta => {
            rl.close();
            resolve(resposta);
        });
    });
}

async function main() {
    const pessoas = [];

    for (let i = 0; i < 5; i++) {
        // Ler idade
        let idade;
        while (true) {
            const idadeInput = await perguntar(`Digite a idade da ${i + 1}ª pessoa: `);
            idade = parseInt(idadeInput, 10);
            if (!isNaN(idade) && idade >= 0) break;
            console.log("Idade inválida! Digite um número inteiro não negativo.");
        }

        // Ler sexo
        let sexo;
        while (true) {
            const sexoInput = await perguntar(`Digite o sexo da ${i + 1}ª pessoa (M/F): `);
            sexo = sexoInput.trim().toUpperCase();
            if (sexo === 'M' || sexo === 'F') break;
            console.log("Sexo inválido! Digite 'M' para homem ou 'F' para mulher.");
        }

        pessoas.push({ idade, sexo });
    }

    // a) Quantos homens
    const totalHomens = pessoas.filter(p => p.sexo === 'M').length;

    // b) Quantas mulheres
    const totalMulheres = pessoas.filter(p => p.sexo === 'F').length;

    // c) Média de idade do grupo
    const mediaIdadeGrupo = pessoas.reduce((acc, p) => acc + p.idade, 0) / pessoas.length;

    // d) Média de idade dos homens
    const homens = pessoas.filter(p => p.sexo === 'M');
    const mediaIdadeHomens = homens.length > 0 
        ? homens.reduce((acc, p) => acc + p.idade, 0) / homens.length 
        : 0;

    // e) Quantas mulheres têm mais de 20 anos
    const mulheresMais20 =

Questão 17: 
const readline = require('readline');

// Função para ler entrada do usuário usando Promise
function perguntar(pergunta) {
    const rl = readline.createInterface({
        input: process.stdin,
        output: process.stdout
    });

    return new Promise(resolve => {
        rl.question(pergunta, resposta => {
            rl.close();
            resolve(resposta);
        });
    });
}

async function main() {
    const pessoas = [];

    for (let i = 0; i < 7; i++) {
        // Ler peso
        let peso;
        while (true) {
            const pesoInput = await perguntar(`Digite o peso da ${i + 1}ª pessoa (kg): `);
            peso = parseFloat(pesoInput.replace(',', '.'));
            if (!isNaN(peso) && peso > 0) break;
            console.log("Peso inválido! Digite um número positivo.");
        }

        // Ler altura
        let altura;
        while (true) {
            const alturaInput = await perguntar(`Digite a altura da ${i + 1}ª pessoa (m): `);
            altura = parseFloat(alturaInput.replace(',', '.'));
            if (!isNaN(altura) && altura > 0) break;
            console.log("Altura inválida! Digite um número positivo.");
        }

        pessoas.push({ peso, altura });
    }

    // a) Média de altura do grupo
    const mediaAltura = pessoas.reduce((acc, p) => acc + p.altura, 0) / pessoas.length;

    // b) Quantas pessoas pesam mais de 90Kg
    const acima90kg = pessoas.filter(p => p.peso > 90).length;

    // c) Quantas pessoas que pesam menos de 50Kg tem menos de 1.60m
    const menos50Menos160 = pessoas.filter(p => p.peso < 50 && p.altura < 1.60).length;

    // d) Quantas pessoas que medem mais de 1.90m pesam mais de 100Kg
    const mais190Mais100 = pessoas.filter(p => p.altura > 1.90 && p.peso > 100).length;

    // Exibir resultados
    console.log(`\nResultados:`);
    console.log(`a) Média de altura do grupo: ${mediaAltura.toFixed(2)} m`);
    console.log(`b) Pessoas com mais de 90Kg: ${acima90kg}`);
    console.log(`c) Pessoas com menos de 50Kg e menos de 1.60m: ${menos50Menos160}`);
    console.log(`d) Pessoas com mais de 1.90m e mais de 100Kg: ${mais190Mais100}`);
}

// Executar programa
main();

Questão 18:
const readline = require('readline');

function perguntar(pergunta) {
    const rl = readline.createInterface({
        input: process.stdin,
        output: process.stdout
    });

    return new Promise(resolve => {
        rl.question(pergunta, resposta => {
            rl.close();
            resolve(resposta);
        });
    });
}

async function jogo() {
    const numeroSecreto = Math.floor(Math.random() * 10) + 1; // 1 a 10
    let tentativas = 4;
    let acertou = false;

    console.log("=== JOGO DE ADIVINHAÇÃO ===");
    console.log("O computador escolheu um número entre 1 e 10. Você tem 4 tentativas!");

    for (let i = 1; i <= tentativas; i++) {
        const chuteInput = await perguntar(`Tentativa ${i}: Digite seu número: `);
        const chute = parseInt(chuteInput, 10);

        if (isNaN(chute) || chute < 1 || chute > 10) {
            console.log("Número inválido! Digite um inteiro entre 1 e 10.");
            i--; // não conta como tentativa
            continue;
        }

        if (chute === numeroSecreto) {
            console.log(`Parabéns! Você acertou o número ${numeroSecreto} na tentativa ${i}!`);
            acertou = true;
            break;
        } else if (chute < numeroSecreto) {
            console.log("O número secreto é maior.");
        } else {
            console.log("O número secreto é menor.");
        }
    }

    if (!acertou) {
        console.log(`\nFim de jogo! O número secreto era: ${numeroSecreto}`);
    }
}

// Iniciar o jogo
jogo();



