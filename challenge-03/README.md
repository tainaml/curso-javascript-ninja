# Desafio da semana #3

```js
// Declarar uma variável qualquer, que receba um objeto vazio.

var variavel = pessoa { }

/*
Declarar uma variável `pessoa`, que receba suas informações pessoais.
As propriedades e tipos de valores para cada propriedade desse objeto devem ser:
- `nome` - String
- `sobrenome` - String
- `sexo` - String
- `idade` - Number
- `altura` - Number
- `peso` - Number
- `andando` - Boolean - recebe "falso" por padrão
- `caminhouQuantosMetros` - Number - recebe "zero" por padrão
*/


var pessoa = {
                 nome: 'taina',
                 sobrenome: 'ml',
                 sexo: 'feminino',
                 idade: '31',
                 altura:'1.70',
                 peso:'80',
                 andando: false,
                 caminhouQuantosMetros: '0'
            }

/*
Adicione um método ao objeto `pessoa` chamado `fazerAniversario`. O método deve
alterar o valor da propriedade `idade` dessa pessoa, somando `1` a cada vez que
for chamado.
*/


var pessoa = {
                 nome: 'taina',
                 sobrenome: 'ml',
                 sexo: 'feminino',
                 idade: '31',
                 altura:'1.70',
                 peso:'80',
                 andando: false,
                 caminhouQuantosMetros: '0'
                 }
                 pessoa.fazerAniversario = function() {
                   pessoa.idade++;
                 }
            

/*
Adicione um método ao objeto `pessoa` chamado `andar`, que terá as seguintes
características:
- Esse método deve receber por parâmetro um valor que representará a quantidade
de metros caminhados;
- Ele deve alterar o valor da propriedade `caminhouQuantosMetros`, somando ao
valor dessa propriedade a quantidade passada por parâmetro;
- Ele deverá modificar o valor da propriedade `andando` para o valor
booleano que representa "verdadeiro";
*/


                 pessoa.andar = function (metros) {
                   pessoa.caminhouQuantosMetros = pessoa.caminhouQuantosMetros + metros
                   pessoa.caminhouQuantosMetros
                   pessoa.andando = true
                 }
            

/*
Adicione um método ao objeto `pessoa` chamado `parar`, que irá modificar o valor
da propriedade `andando` para o valor booleano que representa "falso".
*/


 pessoa.parar = function () {
                   pessoa.andando = false
                 }

/*
Crie um método chamado `nomeCompleto`, que retorne a frase:
- "Olá! Meu nome é [NOME] [SOBRENOME]!"
*/

pessoa.nomeCompleto = function() {
                    return "Olá! Meu nome é " + this.nome + "  " + this.sobrenome
                  }

/*
Crie um método chamado `mostrarIdade`, que retorne a frase:
- "Olá, eu tenho [IDADE] anos!"
*/

  pessoa.mostrarIdade = function() {
              return pessoa.idade
            }

/*
Crie um método chamado `mostrarPeso`, que retorne a frase:
- "Eu peso [PESO]Kg."
*/

pessoa.euPeso = function() {
              return "Eu peso "+ pessoa.peso + "Kg."
            }

/*
Crie um método chamado `mostrarAltura` que retorne a frase:
- "Minha altura é [ALTURA]m."
*/

pessoa.mostrarAltura = function() {
              return "Minha altura é " + pessoa.altura + "m."
            }

/*
Agora vamos brincar um pouco com o objeto criado:
Qual o nome completo da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/

pessoa.nomeCompleto() //'Olá! Meu nome é taina  ml'

/*
Qual a idade da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/

pessoa.mostrarIdade() // '31'

/*
Qual o peso da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/

pessoa.euPeso() // 'Eu peso 80Kg.'

/*
Qual a altura da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/

pessoa.mostrarAltura() // 'Minha altura é 1.70m.'

/*
Faça a `pessoa` fazer 3 aniversários.
*/

pessoa.fazerAniversario()
pessoa.fazerAniversario()
pessoa.fazerAniversario()
                             
                             

/*
Quantos anos a `pessoa` tem agora? (Use a instrução para responder e
comentários inline ao lado da instrução para mostrar qual foi a resposta
retornada)
*/

pessoa.fazerAniversario() //'32'
pessoa.fazerAniversario() // '33'
pessoa.fazerAniversario() // '34

/*
Agora, faça a `pessoa` caminhar alguns metros, invocando o método `andar` 3x,
com metragens diferentes passadas por parâmetro.
*/
 pessoa.andar(10)
 pessoa.andar(20)
 pessoa.andar(40)
 
/*
A pessoa ainda está andando? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
 pessoa.andar(10) // 10
 pessoa.andar(20) // 30
 pessoa.andar(40) // 70
 
/*
Se a pessoa ainda está andando, faça-a parar.
*/
pessoa.parar = function () {
                   pessoa.andando = false
                 }

/*
E agora: a pessoa ainda está andando? (Use uma instrução para responder e
comentários inline ao lado da instrução para mostrar a resposta retornada)
*/

pessoa.andando //false

/*
Quantos metros a pessoa andou? (Use uma instrução para responder e comentários
inline ao lado da instrução para mostrar a resposta retornada)
*/

pessoa.caminhouQuantosMetros // '300'

/*
Agora vamos deixar a brincadeira um pouco mais divertida! :D
Crie um método para o objeto `pessoa` chamado `apresentacao`. Esse método deve
retornar a string:
- "Olá, eu sou o [NOME COMPLETO], tenho [IDADE] anos, [ALTURA], meu peso é [PESO] e, só hoje, eu já caminhei [CAMINHOU QUANTOS METROS] metros!"

Só que, antes de retornar a string, você vai fazer algumas validações:
- Se o `sexo` de `pessoa` for "Feminino", a frase acima, no início da
apresentação, onde diz "eu sou o", deve mostrar "a" no lugar do "o";
- Se a idade for `1`, a frase acima, na parte que fala da idade, vai mostrar a
palavra "ano" ao invés de "anos", pois é singular;
- Se a quantidade de metros caminhados for igual a `1`, então a palavra que
deve conter no retorno da frase acima é "metro" no lugar de "metros".
- Para cada validação, você irá declarar uma variável localmente (dentro do
método), que será concatenada com a frase de retorno, mostrando a resposta
correta, de acordo com os dados inseridos no objeto.
*/
?

// Agora, apresente-se ;)

var pessoa = {
                 nome: 'taina',
                 sobrenome: 'ml',
                 sexo: 'feminino',
                 idade: '1',
                 altura:'1.70',
                 peso:'70',
                 andando: false,
                 caminhouQuantosMetros: 0
            }

            pessoa.euPeso = function() {
              return "Eu peso "+ pessoa.peso + "Kg."
            }

            pessoa.mostrarAltura = function() {
              return "Minha altura é " + pessoa.altura + "m."
            }

            pessoa.nomeCompleto = function() {
                    return this.nome + "  " + this.sobrenome
                  }

            pessoa.mostrarIdade = function() {
              return pessoa.idade
            }

            pessoa.fazerAniversario = function() {
                   return pessoa.idade++
                 }

           pessoa.andar = function (metros) {
                   pessoa.caminhouQuantosMetros = pessoa.caminhouQuantosMetros + metros
                   pessoa.andando = true
                 }

            pessoa.parar = function () {
                   pessoa.andando = false
                 }

            pessoa.apresentacao = function () {
              if (pessoa.sexo === 'feminino') {
                 var nome =  "Olá, eu sou a "
              }else if (pessoa.sexo === 'masculino') {
                return "Olá, eu sou o "
              } // aqui
              if (pessoa.idade === '1') {
                var ano =  " ano"
              }else if (pessoa.idade >= '1'){
                var ano =  " anos"
              }
              if (pessoa.caminhouQuantosMetros === 1) {
                var metro = "metro"
              }else {
                var metro = "metros"
              }
              return nome + pessoa.nomeCompleto() + ", tenho " + pessoa.idade + ano + "e " + pessoa.altura + "m, " + "meu peso é " + pessoa.peso + ",e só hoje, eu já caminhei " + pessoa.caminhouQuantosMetros + " " + metro + "!"
            }

            pessoa.apresentacao() // 'Olá, eu sou a taina  ml, tenho 1 anoe 1.70m, meu peso é 70,e só hoje, eu já caminhei 100 metros!'



```
