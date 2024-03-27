# Unifor - Lista de Exercícios 01
 **Nome:** Vinicius Albuquerque <br>
 **Matrícula:** 2417683 <br>
 **Disciplina:** Raciocínio Lógico Algorítmico <br>
 **Professor:** Ricardo Carubbi <br>

 
 ← 
## Questão 01
### Pseudocódigo
```
1. ALGORITMO trocar_valores
2. INICIO
3.     DECLARE a, b, aux: REAL
4.     ESCREVA "Digite o valor de a: "
5.     LEIA a
6.     ESCREVA "Digite o valor de b: "
7.     LEIA b
8.     aux ← a
9.     a ← b
10.    b ← aux
11.    ESCREVA "Novo valor de a:", a
12.    ESCREVA "Novo valor de b:", b
13. FIM_ALGORITMO
```
### Teste de mesa
| Passo | a   | b   | aux | Mensagem                 |
|-------|-----|-----|-----|--------------------------|
| 3     | 3   | 7   | -   | -                        |
| 8     | 3   | 7   | 3   | -                        |
| 9     | 7   | 7   | 3   | -                        |
| 10    | 7   | 3   | 3   | -                        |
| 11    | 7   | 3   | 3   | "Novo valor de a: 7"     |
| 12    | 7   | 3   | 3   | "Novo valor de b: 3"     |



## Questão 02
### Pseudocódigo
```
1. ALGORITMO contar_aprovados
2. DECLARE n, nota, cont: INTEIRO
3. INICIO
4.     ESCREVA "Digite o número de notas a serem processadas:"
5.     LEIA n
6.     cont ← 0
7.     PARA i DE 1 ATÉ n FAÇA
8.         ESCREVA "Digite a nota do aluno ", i, ":"
9.         LEIA nota
10.        SE nota >= 50 ENTAO
11.            cont ← cont + 1
12.        FIM_SE
13.    FIM_PARA
14.    ESCREVA "O número total de alunos aprovados é:", cont
15. FIM_ALGORITMO

```
### Teste de mesa
| Notas (n) | Nota 1 | Nota 2 | ... | Nota n | Contagem de Aprovados (cont)  |
| --------- | ------ | ------ | --- | ------ | ----------------------------- |
| 5         | 65     | 30     | ... | 55     | 3                             |
| 10        | 40     | 60     | ... | 45     | 7                             |
| 3         | 55     | 45     | ... | -      | 1                             |


## Questão 03
### Pseudocódigo
```
1. ALGORITMO calcular_soma
2. DECLARE n, numero, soma: INTEIRO
3. INICIO
4.     ESCREVA "Digite a quantidade de números a serem somados:"
5.     LEIA n
6.     SE n < 0 ENTAO
7.         ESCREVA "O número de números a serem somados deve ser maior ou igual a zero."
8.     SENAO
9.         soma ← 0
10.        PARA i DE 1 ATÉ n FAÇA
11.            ESCREVA "Digite o número ", i, ":"
12.            LEIA numero
13.            soma ← soma + numero
14.        FIM_PARA
15.        ESCREVA "A soma dos ", n, " números é:", soma
16.    FIM_SE
17. FIM_ALGORITMO

```
### Teste de mesa
| n   | Números           | Soma  |
| --- | ----------------- | ----- |
| 5   | 10, 20, 5, 15, 25 | 75    |
| 3   | 3, -5, 8          | 6     |
| 2   | 0, 0              | 0     |



## Questão 04
### Pseudocódigo
```
1. ALGORITMO calcular_valor_S
2. DECLARE n, i, numerador, denominador: INTEIRO
3. DECLARE termo, S: REAL
4. INICIO
5.     ESCREVA "Digite o número de termos da série:"
6.     LEIA n
7.     SE n < 1 ENTAO
8.         ESCREVA "O número de termos deve ser pelo menos 1."
9.     SENAO
10.        S ← 0
11.        PARA i DE 1 ATÉ n FAÇA
12.            numerador ← 2 * i - 1
13.            denominador ← 2 * i
14.            termo ← numerador / denominador
15.            S ← S + termo
16.        FIM_PARA
17.        ESCREVA "O valor da série S é:", S
18.    FIM_SE
19. FIM_ALGORITMO

```
### Teste de mesa
| n   | Valor de S  |
| --- | ----------- |
| 1   | 0.5         |
| 2   | 1.166666667 |
| 3   | 1.783333333 |


## Questão 05
### Pseudocódigo
```
1. ALGORITMO calcular_fatorial
2. DECLARE n, i, fator: INTEIRO
3. INICIO
4.     ESCREVA "Digite um número inteiro não negativo:"
5.     LEIA n
6.     SE n < 0 ENTAO
7.         ESCREVA "O número deve ser não negativo."
8.     SENAO
9.         fator ← 1
10.        PARA i DE 1 ATÉ n FAÇA
11.            fator ← fator * i
12.        FIM_PARA
13.        ESCREVA "O fatorial de", n, "é", fator
14.    FIM_SE
15. FIM_ALGORITMO
```
### Teste de mesa
| n   | fator | i | Resultado                                      |
|-----|-------|---|------------------------------------------------|
| -2  | -     | - | -                                              |
| -2  | -     | - | "O número deve ser não negativo."              |
| 5   | -     | - | -                                              |
| 5   | 1     | - | -                                              |
| 5   | 1     | 1 | -                                              |
| 5   | 1     | 2 | -                                              |
| 5   | 2     | 3 | -                                              |
| 5   | 6     | 4 | -                                              |
| 5   | 24    | 5 | -                                              |
| 5   | 120   | - | "O fatorial de 5 é 120"                        |


## Questão 06
### Pseudocódigo
```
1. ALGORITMO fibonacci
2. DECLARE n, a, b, termo_atual: INTEIRO
3. INICIO
4.     ESCREVA "Digite o número de termos da sequência de Fibonacci:"
5.     LEIA n
6.     SE n < 1 ENTAO
7.         ESCREVA "O número de termos deve ser pelo menos 1."
8.     SENAO
9.         SE n == 1 ENTAO
10.            ESCREVA "Os primeiros", n, "termos da sequência de Fibonacci são: 0"
11.        SENAO
12.            ESCREVA "Os primeiros", n, "termos da sequência de Fibonacci são: 0, 1"
13.            a ← 0
14.            b ← 1
15.            PARA i DE 3 ATÉ n FAÇA
16.                termo_atual ← a + b
17.                ESCREVA ", ", termo_atual
18.                a ← b
19.                b ← termo_atual
20.            FIM_PARA
21.        FIM_SE
22.    FIM_SE
23. FIM_ALGORITMO
```


## Questão 07
### Pseudocódigo
```
1. ALGORITMO inverter_numero
2. DECLARE num, num_inv, digito: INTEIRO
3. INICIO
4.     ESCREVA "Digite um número inteiro positivo:"
5.     LEIA num
6.     SE num < 0 ENTAO
7.         ESCREVA "O número deve ser positivo."
8.     SENAO
9.         num_inv ← 0
10.        ENQUANTO num > 0 FAÇA
11.            digito ← num % 10
12.            num_inv ← num_inv * 10 + digito
13.            num ← num / 10
14.        FIM_ENQUANTO
15.        ESCREVA "O número invertido é: ", num_inv
16.    FIM_SE
17. FIM_ALGORITMO
```
