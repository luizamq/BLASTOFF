# Teste de Lógica - Seleção Programa Blastoff
### Teste de Lógica com 14 questões, parte do processo seletivo para o programa Blastoff na empresa Toodoo.

Oi, time Toodoo! Sou Luiza Moruz e esse é o resultado do meu teste de lógica. Obrigada pela oportunidade de fazer esse desafio! Achei desafiador na medida certa e até divertido de fazer! :)
A linguagem que escolhi para fazer foi Swift, pois é que a venho estudando nos ultimos meses e tenho mais familiaridade! E também porque eu amo a praticidade da sintaxe do Swift!
### Observação importante: como no Swift Playground é impossível ler um input, eu atribui valores numéricos em todas as questões. No arquivo Contents.swift talvez seja mais fácil de ler os códigos! :)

### Resultado:

#### Questão 01) Dada as idades I, J, K, X, Y, faça um algoritmo para calcular a média das idades
```
//Considerando os valores inteiros I=10; J=15, K=20, X=25 e Y=30;

let idadesFamilia = [
    "I": 10,
    "J": 15,
    "K": 20,
    "X": 25,
    "Y": 30 ]

let somaIdades = idadesFamilia.values.reduce(0, +)

let pessoasFamilia = idadesFamilia.count
let mediaIdades = somaIdades / pessoasFamilia

print("Questão 01) A média de idade dessa família é de \(mediaIdades) anos")
```

#### Questão 02) Dada a distância A e o combustível gasto B, faça um algoritmo para calcular o consumo médio:
```
Considerando os valores do tipo Float (Real) A = 290Km e B= 18 L;

let distanciaPercorrida:Float = 290
let combustivelGasto:Float = 18

var consumoMedio:Float = Float(distanciaPercorrida / combustivelGasto)

print("Questão 02) Para esse caso, o consumo médio foi de aproximadamente \(consumoMedio.rounded(.up))km por litro de combustível.")
```

#### Questão 03) Dados três números (a, b, c), faça um algoritmo para mostrar o menor número.
```
let a = 98
let b = 54
let c = 13

let numeros = [a, b, c]
let minNumero = numeros.min()

print("Questão 03) O menor numero declarado foi \(minNumero!).")
```

#### Questão 04) Faça um algoritmo que converta a temperatura de C para F. Utilize a fórmula C=5/9(F-32)
```
//Obs: no Swift Playground é impossível ler um input, nesse caso, o input seria a temperatura em Celsius que se quer transformar. Para esse caso, determinei 40 graus Celsius para fazer o algoritmo.
    
func converterTemp(celsius: Double) -> Double {
    var fahrenheit: Double
    
    fahrenheit = celsius*9 / 5 + 32
    return fahrenheit
}

var resultado = converterTemp(celsius: 40)

    print("Questão 04) Essa temperatura é equivalente a \(resultado) graus fahrenheit")
```

#### Questão 05) Faça um algoritmo para apresentar se dois números são multiplos.
```
var primeiroNumero = 7
var segundoNumero = 49

if primeiroNumero.isMultiple(of: segundoNumero) {
    print("Questão 05) Os números são múltiplos")
} else {
    print("Questão 05) Os números não são múltiplos")
}
```

#### Questão 06) Uma partida de futebol iniciou na hora A e terminou na hora B. Faça um algoritmo que calcule o tempo que durou a partida.
```
let horaA = "9:00PM"
let horaB = "11:40PM"
    
let formatacaoHora = DateFormatter()
formatacaoHora.dateFormat = "h:mma"

let dataA = formatacaoHora.date(from: horaA)!
let dataB = formatacaoHora.date(from: horaB)!

let tempoDuracao = dataB.timeIntervalSince(dataA)

let horas = floor(tempoDuracao / 60 / 60)
let minutos = floor((tempoDuracao - (horas * 60 * 60)) / 60)

print("Questão 06) A partida começou 9:00 PM, terminou 11:40PM e durou \(Int(horas)) horas e \(Int(minutos)) minutos")
```

#### Questão 07) Dada uma lista de números A[1,2,3...] faça um algoritmo que retorne uma lista somente com os números pares.
```
//Aqui decidi filtrar os numeros da primeira Array de forma que, divididos por 2, restam 0, ou seja, são números pares.
var listaNumeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

var listaPares = listaNumeros.filter({$0 % 2 == 0})

print("Questão 07) A nova lista com os números pares é: \(listaPares)")
```

#### Questão 08) Faça um algoritmo que receba um número e retorne se o número é primo ou não.
```
//Obs: no Playground é impossível ler um input, nesse caso, o input seria o número que se quer testar ser primo. Para esse caso, determinei o teste do número 631.
let numero = 631
var condicao : Bool = false;

    for i in 2...631/2 {
    if(631 % i == 0){
        condicao = true
        break;
    }
    }
if condicao == false {
    print("Questão 08) O número \(numero) é Primo!")
} else {
    print("Questão 08) O número \(numero) não é Primo!")
}
```

#### Questão 09) Faça um algoritmo que receba um número e retorne a tabuada desse número.
```
// Considerando a tabuada do número 9
var numeroTabuada = 9
    print("Questão 09) A tabuada de \(numeroTabuada) é:")
for i in 0...10 {
    print("\(numeroTabuada) x \(i) = \(i*numeroTabuada)")
}
```

#### Questão 10) Faça um algoritmo que receba um número e retorne o fatorial desse número.
```
func calculoFatorial(num: Int) -> Int {
    var resultadoFatorial = 1
    if(num > 0) {
        for i in 1...num {
            resultadoFatorial *= i
        }
    }
    return resultadoFatorial  
}
    
let numeroFatorar = 9
let resultadoFatoracao = calculoFatorial(num: numeroFatorar)
    print("Questão 10) O resultado do fatorial de \(numeroFatorar) é \(resultadoFatoracao).")
```

#### Questão 11) Dada duas lista de números A[1,2,3,4] e B[1,2,5,8], faça um algoritmo que retorne a intersecção das listas.
```
var primeiraLista : Set = [1, 2, 3, 4]
var segundaLista : Set = [1, 2, 5, 8]

var interseccao = primeiraLista.intersection(segundaLista).sorted()

print("Questão 11) A intersecção das listas A e B é a lista: \(interseccao)")
```

#### Questão 12) Dada duas lista de números A[1,2,3,4] e B[1,2,5,8], faça um algoritmo que retorne a concatenação das listas.
```
var listaA : Array = [1, 2, 3, 4]
var listaB : Array = [1, 2, 5, 8]

var concatenacao = listaA + listaB

print("Questão 12) A concatenação das listas A e B é: \(concatenacao)")
```

#### Questão 13) Faça um algoritmo que receba uma matriz[i,z] como parâmetro e imprima todos os valores dessa matriz.
```
print("Questão 13) O retorno do algoritmo foi:")
var matriz = ["Luiza", "Moruz"]

func nomeCompleto(nomes: Array<String>) {
    for nomes in nomes {
         print(nomes)
    }
}

nomeCompleto(nomes: matriz)
```

#### Questão 14) Faça um algoritmo que recebe uma palavra e retorne se a palavra é palíndromo.
```
var palavra : String = "reviver"
var palavraContrario = String(palavra.reversed())

if palavra == palavraContrario {
    print("Questão 14) A palavra \(palavra) é um palíndromo")
    } else {
        print("Questão 14) A palavra \(palavra) não é um palíndromo")
}
```
### Resultado no Console do Swift Playground:

![image](https://user-images.githubusercontent.com/90458139/138296688-763efe9a-1d0a-40b9-a69c-24b78fa22e85.png)
