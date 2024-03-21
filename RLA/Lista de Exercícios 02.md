# Unifor - Lista de Exercícios 02
 **Nome:** Vinicius Albuquerque <br>
 **Matrícula:** 2417683 <br>
 **Disciplina:** Raciocínio Lógico Algorítmico <br>
 **Professor:** Ricardo Carubbi <br>

## Exercício 1 
### Fluxograma
```mermaid
flowchart TD
    Inicio((INÍCIO)) --> Numero1[/Digite o primeiro número:/]
    Numero1 --> Numero2[/Digite o segundo número/]
    Numero2 --> Numero3[/Digite o terceiro número:/]
    Numero3 --> Numero4[/Digite o quarto número:/]
    Numero4 --Calcular a média dos números--> CalcularMedia([Somar o primeiro número com o segundo,com o terceiro <br> e com o quarto números e, depois, divida o resultado dessa <br> soma por 4.])
    CalcularMedia --Média--> ResultadoMedia[O resultado da sua média é:]
    ResultadoMedia --> Fim((FIM))
```
### Pseudocódigo
```
1. ALGORITMO calcular_media
2. DECLARE numero1, numero2, numero3, numero4: REAL
3. DECLARE media: POSITIVO
4. ESCREVA "Digite o primeiro número: "
5. INICIO
6.     LEIA numero1
7.     ESCREVA "Digite o segundo número: "
8.     LEIA numero2
9.     ESCREVA "Digite o terceiro número: "
10.    LEIA numero3
11.    ESCREVA "Digite o quarto número: "
12.    LEIA numero4
13.    media = (numero1 + numero2 + numero3 + numero4) % 4
14.    ESCREVA "A média dos números é: ", media
15. FIM_ALGORITMO
```
### Teste de Mesa
| numero1 | numero2 | numero3 | numero4 | soma | media |
| -- | -- | -- | -- | -- | -- |
| 16 | (-8) | (-5) | 1 | 4 | 1 |
| 2 | 6 | 10 | (-8) | 10 | 2,5 |
| 12 | 3 | 5 | (-20) | 0 | 0|
| 0 | 9 | 106 | 5 | 120 | 30|


## Exercício 2
### Fluxograma
```mermaid
flowchart TD
    Inicio((INÍCIO)) -->Celsius[/Digite a temperatura em Celsius:/]
    Celsius -->CalcularFahrenheit([Calcular temperatura em Fahrenheit])
    CalcularFahrenheit --> MostrarFahrenheit[Mostrar temperatura em Fahrenheit]
    MostrarFahrenheit --> Fim((FIM))
```
### Pseudocódigo
```
1. ALGORITMO converter_Celsius_Fahrenheit
2. DECLARE celsius, fahrenheit: REAL
3. ESCREVA "Digite a temperatura em Celsius: "
4. INICIO
5.     LEIA celsius
6.     fahrenheit = (9/5) * celsius + 32
7.     ESCREVA "A temperatura em Fahrenheit é: ", fahrenheit
8. FIM_ALGORITMO
```
### Teste de Mesa
| Celsius | Fórmula                     | Fahrenheit |
| ------- | --------------------------- | -- |
| -10     | (9/5) * (-10) + 32 = 14     | 14 |
| 0       | (9/5) * 0 + 32 = 32         | 32 |
| 25      | (9/5) * 25 + 32 = 77        | 77 |
| 100     | (9/5) * 100 + 32 = 212      | 212|


## Exercício 03
### Fluxograma
```mermaid
flowchart TD
    Inicio((INÍCIO)) --> NumerosOperador[/Digite os dois números reais e o operador:/]
    NumerosOperador --SE + - * %--> CalcularOP[Calcular a operação selecionada]
    NumerosOperador --SENÃO--> OperadorValido[/Digite um operador válido/]
    OperadorValido --> CalcularOP
    CalcularOP --Resultado--> MostrarResultado[O resultado da operacao é:]
    MostrarResultado --> Fim((FIM))
```
### Pseudocódigo
```
1. ALGORITMO calcular_operacao
2. DECLARE numero1, numero2, resultado: REAL
3. DECLARE operador: CARACTERE
4. INICIO
5.     ESCREVA "Digite os dois números reais e o operador: "
6.     LEIA numero1, numero2, operador
7.     ESCOLHA operador
8.         SE "+"
9.             resultado = numero1 + numero2
10.        SE "-"
11.            resultado = numero1 - numero2
12.        SE "*"
13.            resultado = numero1 * numero2
14.        SE "/"
15.            resultado = numero1 / numero2
16.        SENÃO
17.            ESCREVA "Digite um operador valido!"
18.    FIM_ESCOLHA
19.    ESCREVA "O resultado da operação é: ", 'resultado'"
20. FIM_ALGORITMO

```
### Teste de Mesa
| numero1 | numero2  | Operador | Operação   | Resultado        |
| -- | -- | -------- | ---------------------| ----------------- |
| 5  | 3  | +        | 5 + 3 = 8            | 8                 |
| 10 | 9  | -        | 10 - 2 = 8           | 1                 |
| 4  | 6  | *        | 4 * 6 = 24           | 24                |
| 12 | 4  | /        | 12 / 4 = 3           | 3                 |


## Exercício 04
### Fluxograma
```mermaid
flowchart TD
    Inicio((INÍCIO)) --> Idade[/Digite a idade:/]
    Idade --> ClassificarIdade([Classificar a idade em categorias])
    ClassificarIdade --Categoria--> MostrarCategoria[Mostrar a categoria correspondente]
    MostrarCategoria --> Fim((FIM))
```
### Pseudocódigo
```
1. ALGORITMO classificar_idade
2. DECLARE idade: INTEIRO
3. INICIO
4.     ESCREVA "Digite a idade: "
5.     LEIA idade
6.     SE idade >= 5 E idade <= 7 ENTÃO
7.         ESCREVA "Categoria: Infantil A"
8.     SE idade >= 8 E idade <= 10 ENTÃO
9.         ESCREVA "Categoria: Infantil B"
10.    SE idade >= 11 E idade <= 13 ENTÃO
11.        ESCREVA "Categoria: Juvenil A"
12.    SE idade >= 14 E idade <= 17 ENTÃO
13.        ESCREVA "Categoria: Juvenil B"
14.   SENÃO
15.       ESCREVA "Categoria: Adulto"
16.    FIM_SE
17. FIM

```
### Teste de Mesa
| Idade | Categoria     | Categoria             |
| ----- | ------------- | --------------------- |
| 6     | Infantil A    | Categoria: Infantil A |
| 9     | Infantil B    | Categoria: Infantil B |
| 12    | Juvenil A     | Categoria: Juvenil A  |
| 16    | Juvenil B     | Categoria: Juvenil B  |
| 20    | Adulto        | Categoria: Adulto     |


