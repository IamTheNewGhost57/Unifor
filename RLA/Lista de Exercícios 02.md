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
