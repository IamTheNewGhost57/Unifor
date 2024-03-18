# Unifor - Lista de Exercícios 01
**Nome:** Vinicius Albuquerque
**Disciplina:** Raciocínio Lógico Algorítmico

## Exercício 1 
### Fluxograma

```mermaid
flowchart TD  
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
```
### Pseudocódigo
```
1  ALGORÍTMO verifica_par_ímpar
2  DECLARE número, resto NUMÉRICO
3  ESCREVA "Digite um número"
4  LEIA número
5  SE número > 0
6     resto = número % 2
7     SE resto == 0 ENTÃO
8        ESCREVA "O número é par!"
9     SENÃO
10       ESCREVA "O número não é ímpar!"
11  SENÃO
12    ESCREVA "O número não é positivo"
13  FIM_ALGORÍTMO 
```
### Teste de mesa
| Número | Número >= 0 | resto | resto == 0 | Mensagem                      |
| --     | --          | --    | --         | --                            | 
| -1     | F           |       |            | "O número deve ser postivo!"  |
| 0      | V           | 0     | V          | "O número é par!"             |
| 13     | V           | 1     | F          | "O número é ímpar!"           |
| 30     | V           | 0     | V          | "O número é par!"             |


## Exercício 2 
### Fluxograma
```mermaid
flowchart TD
    A((INÍCIO)) --> I[/Digite o salário do funcionário:/]
    I --> B{{Salário Atual}}
    B --Salário <= 500--> D{Aumento de 20%}
    B --Salário > 500--> C{Aumento de 10%}
    C --> G[Novo Salário = Salário Atual * 1.10]
    G --> H
    D --> E[Novo Salário = Salário Atual * 1.20]
    E --> H((FIM))
```
### Pseudocódigo
```
1 ALGORITMO calcula_aumento_salário
2 DECLARE salario, novo_salario: REAL
3 ESCREVA "Digite o salário atual do funcionário: "
4 INICIO
5     LEIA salario
6     SE salario <= 500 ENTAO
7         novo_salario = salario * 1.20
8     SENÃO
9         novo_salario = salario * 1.10
10    FIM_SE
11    ESCREVA "Novo salário do funcionário: ", novo_salario
12 FIM_ALGORITMO
```

### Teste de mesa

| Salário Atual| Salário Atual <= 500 | Novo Salário                               | 
|      --      |      --              |      --                                    |
| R$ 501.00    | F                    | Multiplique o Salário Atual por 1.10       |
| R$ 500.00    | V                    | Multiplique o Salário Atual por 1.20       |
| R$ 499.00    | V                    | Multiplique o Salário Atual por 1.20       |


