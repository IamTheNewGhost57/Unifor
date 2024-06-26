# Unifor - Lista de Exercícios 01
 **Nome:** Vinicius Albuquerque <br>
 **Matrícula:** 2417683 <br>
 **Disciplina:** Raciocínio Lógico Algorítmico <br>
 **Professor:** Ricardo Carubbi <br>

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
1  ALGORITMO verificar_par_ímpar
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
13  FIM_ALGORITMO 
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
1 ALGORITMO calcular_aumento_salário
2 DECLARE salario, novo_salario: REAL, POSITIVO
3 ESCREVA "Digite o salário atual do funcionário: "
4 INICIO
5     LEIA salario
6     SE salario <= 500 ENTAO
7         novo_salario = salario * 1.20
8     SENÃO
9         novo_salario = salario * 1.10
10    FIM_SE
11 ESCREVA "Novo salário do funcionário: ", novo_salario
12 FIM_ALGORITMO
```
### Teste de mesa

| Salário Atual| Salário Atual <= 500 | Novo Salário                               | 
|      --      |      --              |      --                                    |
| R$ 501.00    | F                    | Multiplique o Salário Atual por 1.10       |
| R$ 500.00    | V                    | Multiplique o Salário Atual por 1.20       |
| R$ 499.00    | V                    | Multiplique o Salário Atual por 1.20       |


## Exercício 3 
### Fluxograma
```mermaid
flowchart TD
    Inicio((INÍCIO)) --> Nota1[/Digite a primeira nota do aluno:/]
    Nota1 --> Nota2[/Digite a segunda nota do aluno:/]
    Nota2 --Calcular a média das notas--> ResultadoMédia[ Some nota 1 + nota 2, depois divida o resultado da soma por 2.]
    ResultadoMédia --> Situacao[Verificar a média do aluno]
    Situacao --Média >= 7--> Aprovado[Situação: Aluno Aprovado]
    Situacao --Média < 7--> Reprovado[Situação: Aluno Reprovado]
    Aprovado --> Fim((FIM))
    Reprovado --> Fim
```
### Pseudocódigo
```
1. ALGORITMO calcular_media_situacao 
2. DECLARE nota1, nota2, media: REAL, POSITIVO, >0, <=10
3. INICIO
4. ESCREVA "Digite a primeira nota do aluno: " 
5.   LEIA nota1 
6. ESCREVA "Digite a segunda nota do aluno: " 
7.   LEIA nota2 
8. CALCULE media = (nota1 + nota2) % 2 
9.   SE media >= 7
10.    ENTAO, ESCREVA "Situação: Aluno Aprovado"
11.  SENAO 
12.     ESCREVA "Situação: Aluno Reprovado" 
13.  FIM_SE 
14. FIM_ALGORITMO
```
### Teste de mesa
| Primeira nota | Segunda nota | Média | Média >=7 | Situação  | 
|      --       |      --      |   --  |      --   |      --   | 
| 7             | 7            | 7     | V         | Aprovado  |
| 6             | 8            | 7     | V         | Aprovado  |
| 5             | 8            | 6,5   | F         | Reprovado |
| 10            | 2            | 6     | F         | Reprovado |


## Exercício 4
### Fluxograma
``` mermaid
flowchart TD
    INÍCIO((INÍCIO)) --> Idade[/Digite a idade do candidato:/]
    Idade --> VerificarIdade([Verificar se a idade atende ao requisito da CNH])
    VerificarIdade --Idade >= 18--> CNHApto([O candidato pode tirar a CNH])
    VerificarIdade --Idade < 18--> CalcularFaltante([Calcular os anos faltantes para o candidato estar apto])
    CalcularFaltante --Anos Faltantes--> AnosFaltante[Anos faltantes = 18 - A idade do candidato]
    --> Fim([FIM])
    CNHApto --> Fim
```
### Pseudocódigo
```
1. ALGORITMO verificar_CNH_Apto
2. DECLARE idade, anos_faltantes: INTEIRO, POSITIVO
3. ESCREVA "Digite a idade do candidato: "
4. INICIO
5. LEIA idade
6.   SE idade >= 18, ENTAO
7.     ESCREVA "O candidato pode tirar a CNH"
8.   SENAO
9.     anos_faltantes = 18 - idade_candidato
10. ESCREVA "O candidato não pode tirar a CNH. Faltam 'anos_faltantes' anos para estar apto."
11.  FIM_SE
12. FIM
```
### Teste de mesa
| Idade do candidato | Idade >=18   | Anos faltantes | Situação     |
|      --            |      --      |      --        |      --      |
| 19                 | V            | 0              | Apto         |
| 18                 | V            | 0              | Apto         | 
| 17                 | F            | 1              | Não apto     |

