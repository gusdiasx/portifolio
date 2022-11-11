## Funções

#### O que é uma função e pra que servem?

    Uma parte de extrema importância na programação são as funções, a função é um pedaço de código que faz alguma tarefa específica e pode ser chamado de qualquer parte do programa quantas vezes desejarmos, isso evita termos que ficar repetindo linha de código varias vezes para tarefas que são usadas repetidas vezes

Como declarar uma função em python?

O escopo da declaração de uma função é:

    #ff0000 def nome_função (argumentos):

código
return valor

#000000 Não necessariamente ela precisa ter argumentos ou retornar algum valor. E como já dito antes, a indentação é de extrema importância no python!

Uma função simples para o melhor entendimento de vocês:

    def mensagem ():   Aqui definimos a função, observem que ela não possui parâmetros

print ("Olá, mundo")

Observem também que ela não possui um retorno, apenas mostrará algo.

    mensagem ()   Aqui chamamos a função, aqui é onde será executada!

Quando executarmos a função, ele mostrará no terminal a seguinte mensagem:
Olá, mundo

### O que são parâmetros de uma função?

    Os parâmetros são valores que a função irá receber. Muita das vezes é necessária para executar tarefas que devem receber um valor que não faz parte do escopo da função.

Um exemplo para entender melhor:

    def soma (x, y):  Aqui definimos a função
           valorSoma = x + y
           print (“A soma dos parâmetros é: “, valorSoma)

Observem que ela não possui um retorno, apenas mostrará algo.

    soma (5, 9)  Aqui chamamos a função, com seus parâmetros definido

Quando executarmos a função, ele mostrará no terminal a seguinte mensagem:
A soma dos parâmetros é: 14
Como perceberam, utilizamos valores de fora da função para fazer a soma e apresentar no terminal pela função. Os parâmetros são uma ferramenta de muita utilidade, assim como o retorno!

### O que é retorno de uma função e como usar?

    A instrução return serve para retornar/devolver um valor que foi calculado ou formado dentro da função para o chamador da função.

### Um exemplo usando o mesmo código de cima para melhor entendimento:

    def soma (x, y):  Aqui definimos a função
           valorSoma = x + y
           return valorSoma  Aqui retornamos o valor da variável valorSoma

    a = 20
    b = 30
    c= 40
    somaParametros = soma (a, b)  Notem que somaParametros que chama e recebe o valor da função.
    print (“A soma dos parâmetros é: “, somaParametros)
    somaParametros = soma (b, c)  Notem que somaParametros que chama e recebe o valor da função.
    print (“A soma dos parâmetros é: “, somaParametros)

Observem que na chamada da função não é necessário usar os mesmos nomes ou valores da definição da função.
E como agora retornamos o valor para somaParametros executamos o print fora do escopo da função.

Quando executarmos a função, ele mostrará no terminal a seguinte mensagem:
A soma dos parâmetros é: 50
A soma dos parâmetros é: 70

### Outro exemplo pra tentar ajudar vocês a entender melhor:

def area_triangulo (base, altura):
area = (base \* altura)/2
return area

print (“A área do triangulo é: “, area_triangulo (10, 4))
print (“A soma dos parâmetros é: “, area_triangulo (23, 7))
print (“A soma dos parâmetros é: “, area_triangulo (58, 10))

Sim, podemos chamar a função dentro do print, isso foi so um exemplo para mostrar o retorno e como é mais simples fazer o calculo usando a função, ao invés de repetir o código varias vezes.

Caso não usasse a função ficaria assim:

area = (10 _ 4)/2
print (“A soma dos parâmetros é: “, área)  
area = (27 _ 7)/2
print (“A soma dos parâmetros é: “, área)
area = (58 \* 10)/2
print (“A soma dos parâmetros é: “, área)
Nesse caso na verdade o código ficou com e mesma quantidade de linhas, mas é porque a função é bem simples, pode ter certeza que se fosse algo mais complexo, com certeza economizaria muitas linhas de código, além de ficar mais organizado e mais fácil de entender.

Quando executarmos a função, ele mostrará no terminal a seguinte mensagem:

A área do triangulo é: 20
A área do triangulo é: 94.5
A área do triangulo é: 290

Manipulação de String

Uma string herda os métodos da classe String para manipular sua coleção de caracteres. Esses métodos permitem algumas tarefas, dentre elas:

- Obter o seu tamanho ou quantidade de caracteres
- Obter um trecho específico do texto
- Substituir um trecho específico do texto
- Verificar a ocorrência de um trecho específico de texto

######Algumas funções de manupulação de string:

capitalize() -> Coloca a 1ª letra Maiúscula;
casefold() -> Transforma todas as letras em minúsculas (existe lower() mas o casefold é melhor normalmente);
count() -> Conta a quantidade de vezes que um valor/símbolo/letra aparece na string;
find() -> Procura um texto dentro de outro texto e dá como resposta a posição do texto encontrado (lá no início falamos que cada letra/símbolo tem uma posição no texto);
format() -> Formata uma string de acordo com os valores passados;
isalnum() -> Verifica se um texto é todo feito com caracteres alfanuméricos (letras e números) -> letras com acento ou ç são considerados letras para essa função;
isalpha() -> Verifica se um texto é todo feito de letras;
isnumeric() -> Verifica se um texto é todo feito por números;
replace() -> Substitui um texto por um outro texto em uma string;
split() -> Separa uma string de acordo com um delimitador em vários textos diferentes;
splitlines() -> separa um texto em vários textos de acordo com os “enters” do texto;
startswith() -> Verifica se a string começa com determinado texto;
strip() -> Retira caracteres indesejados dos textos. Por padrão, retira espaços “extras” no início e no final;
title() -> Coloca a 1ª letra de cada palavra em maiúscula;
upper() -> Coloca o texto todo em letra maiúscula.

Exemplo de como utilizar as funções de manipulação:

# manipulação de strigs

nome = "tres pratos de trigo PARA tres tigres tristes"

print(nome.capitalize())
print(nome.casefold())
print(nome.count("tres"))
print(nome.find("tigres"))
print(nome.replace("tres", "seis"))
print(nome.split())
print(nome.startswith("tristes"))
print(nome.startswith("tres"))
print(nome.title())
print(nome.upper())

Resultado no terminal:

Tres pratos de trigo para tres tigres tristes
tres pratos de trigo para tres tigres tristes
2
31
seis pratos de trigo PARA seis tigres tristes
['tres', 'pratos', 'de', 'trigo', 'PARA', 'tres', 'tigres', 'tristes']
False
True
Tres Pratos De Trigo Para Tres Tigres Tristes
TRES PRATOS DE TRIGO PARA TRES TIGRES TRISTES
