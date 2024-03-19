# Unifor - Lista de Exercícios 03
 **Nome:** Vinicius Albuquerque <br>
 **Matrícula:** 2417683 <br>
 **Disciplina:** Raciocínio Lógico Algorítmico <br>
 **Professor:** Ricardo Carubbi <br>


## Exercício 01
### Fluxograma
```mermaid
 A([INICIO]) --> B{{Digite um número: }}
  B --> C[/número/]
  C --> D{número > 0}
  D --NÃO--> E[O número não e positivo!]
  D --SIM--> F[resto = número % 2]
  E --> Z([FIM])
  F --> G{resto == 0}
  G --NÃO--> H{{O número é ímpar}}
  G --SIM--> I{{O número é par!}}
  H --> Z
  I --> Z
  Z --LOOP--> A
```
### Pseudocódigo
```
1. ALGORITMO verificar_par_impar
2. DECLARE numero, resto: INTEIRO
3. INICIO
4.     ESCREVA "Digite um número: "
5.     LEIA numero
6.     ENQUANTO numero < 0 FAÇA
7.         ESCREVA "Por favor, digite um número maior ou igual a zero: "
8.         LEIA numero
9.     FIM_ENQUANTO
10.    SE numero % 2 == 0 ENTÃO
11.        ESCREVA numero, " é um número par."
12.    SENÃO
13.        ESCREVA numero, " é um número ímpar."
14.    FIM_SE
15. FIM
```
### Teste de Mesa
| Numero | numero >= 0 | Resultado             |
| ------ | ----------- | --------------------- |
| -5     | False       | Digite um número maior ou igual a zero |
| 0      | True        | 0 é um número par.    |
| 7      | True        | 7 é um número ímpar.  |
| 12     | True        | 12 é um número par.   |


## Exercício 02
### Fluxograma
```mermaid

```
### Pseudocódigo
```

```
### Teste de Mesa


## Exercício 03
### Fluxograma
```mermaid

```
### Pseudocódigo
```

```
### Teste de Mesa



## Exercício 04
### Fluxograma
```mermaid

```
### Pseudocódigo
```

```
### Teste de Mesa
