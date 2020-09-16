
INTRODUÇÃO JAVASCRIPT 

No javascript não precisa declarar a tipagem

mas se for string colocar a atribuição entre ""

Declarando variaves

var nome = Vanessa;
var idade = 26;

ou

var nome = vanessa, idade = 26;

Declarando array

var nome = ['Vanessa', Luis, Carlo, Raquel];

Declarando objetos

var alunos = {
  nome: 'Vanessa',
  idade: 26,
  peso: 47,6,
  humano: true
};

repare que para declar o objeto abrimos {} e colocamos a informação daquele objeto dentro das chaves e as informações dentro dele é a variavel seguida de : a informação a ser armazenada e coloco uma "," para separar de outra informação que desejo inserir a ultima informação não tem a virgula.


Incremento 
x = x + 3 é a mesma coisa que x += 3;

Como pegar o resto de uma divisão

resultado = x % y;

Multiplicação

x *= y

Criar uma função:

Como na variavél colocamo o var antes da variavel, na função colocamos a palavra function antes do nome da função o nome da função é seguigo de () dentro dos parenteses colocamos os parametro desejados para serem recebidos. Enfim retornamos o que queremos após ser feita a operação com o comando return e em seguida a variavel que armazena o valor da resposta que queremos retornar.

Fora da função definimos novamente a variavel e atribuimos a função a ele; 

Exemplo:

function soma(numero1, numero2) {
      var resultado = numero1 + numero2;

      return resultado;
    }

    var resultado = soma(1,2);

Sinais

 == faz o comparativo dos valores, para saber se são iguais. 
 === faz o comparativo se os tipos das variaves são iguais além de fazer o comparativo se elas tem ou não os valores iguais.

 Use o switch caso queira verificar o valor de uma variavel multiplas vezes:

 function retornaSexo(sexo) {
      switch (sexo) {
        case 'M':return 'Masculino';
        case 'F':return 'Feminino';
        default:return 'Outro'; Esse ultimo é caso não seja nenhum dos anteriores
      }
    }


Usando AND, OR, NOT

AND é definido pelo simbulo && 
var sexo = 'M', idade = 23;

    if (sexo === 'M' && idade >= 18) { 
      console.log('OK');
    }

AND é definido pelo simbulo ||

 var sexo = 'M', idade = 23;

    if (sexo === 'M' || idade >= 18) { 
      console.log('OK');
    }

AND é definido pelo simbulo !== ou != 

 var sexo = 'F';


    if (sexo !== 'M'){
      console.log('OK')
    }

var sexo = 'F';

    if (sexo != 'M'){
      console.log('OK')
    }

compara a desigualdade das variaveis.


Comparativos:

Podemos usar o código abaixo

Se o sexo for igual a M retorna verdadeiro se não retorna falso


var sexo = 'M';
var masculino;

if (sexo === 'M') {
     masculino = true;
    } else {
     masculino = false;
    }

ou podemos usar o código abaixo que faz a mesma coisa, a varialvel também consegue armazenar uma condição e retornar se é verdadeira ou falsa

var sexo = 'F';

    var masculino = sexo === 'M';

    console.log(masculino);
  

  Condição Ternária

  Quando temos duas verificações dentro do if, um if e logo após um else:

  var sexo = 'M';

    if (sexo === 'M') {
      return 'Masculino';
    } else {
      return 'Feminino';
    }

  mas para escrever de formaternaria e para o código ficar menos verboso podemos escreve-lo dessa forma e o resultado será o mesm:

  var sexo = 'M';
  
  var retorno = (sexo === 'M') ? 'Masculino' : 'Feminino';

  Declaramos a variavel retorno e logo após colocamos a condição (sexo === 'M'), depois com o sinal de "?" fazemos a pergunta, o sinal significa o se=if. Se sexo for igual a 'M' retorna 'Masculino' se não retorna 'Feminino', neste caso o senão=else é representado pelos ":". A primeira condição será sempre a verdadeira que é colocada logo após o "?" a segunda que vem após ":" é a falsa. 

Estruturas de repetição for e while

Usamos o for quando sabemos onde queremos chegar por exemplo contar de 1 até 100, já o while quando não sabemos exatamente quando aquilo será executado, por exemplo quando temos um valor muito grande e não sabemos quantas vezes precisaremos execuar para dividir esse numo, segue abaixo exemplos:

Colocamos o for e logo após dentro dos parentes determinamos que o i é igual a 0, após o ";" colocamos a condição, enquando o i for menor ou igua "<=" a 100 ele vai adicionar mais um que é determinado logo após o ";" i++(incremento). Teremos todos os numeros até chegar no 100.

for (var i  = 0; i <= 100; i++) {
      console.log(i);
    }


Definimos um valor aleatório para j e dentro do while colocamos a condição de que se j for maior que 50 será feita a execução de dentro das chaves, que é dividir o j por 5. Observe que é dificil definir quantas vezes será feita essa execução já que o valor de j é muito grade e é nesses casos que se usa o while diferente de quando usamos o "for" que sabemos exatamente qual será a quantidade de execução ou de intervalo que serão feitos. 

var j = 545645145;
while (j > 50) {
  console.log(j);
  j /= 5;
}

Intervalo e timeout

O intervalo no javascrip é uma função onde ela executa varias vezes dentro de um intervalo.

Abaixo foi criada a função exibAlgo e dentro dela apena pede para exibir o Hello Word, logo abaixo fora da função temos o setIntervalo dentro dela colocamos como parametro a função exibeAlgo sem o () para ela não executar somente passar a função exibeAlgo e depois da "," foi colocada o 1000 que sgnifica o intervalo que eu quero que a função passada como parametro seja executada, dessa forma a cada 1 segundo será execudada a função exibeAlgo mostarando o Hello Word.


function exibeAlgo(){
      console.log('Hello Word');
    }
    setInterval(exibeAlgo, 1000)


Já o Timeout executa apena uma vez a função que foi passada como parametro dando apenas um delay para executar a função.

No exemplo abaixo a função exibeAlgo será executada uma vez após 5 segundos atrávés da função setTimeout:

    function exibeAlgo(){
      console.log('Helo Word');
    }
    setTimeout(exibeAlgo, 5000)

