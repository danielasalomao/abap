# Abap

## Estruturas de condições e Loops SAP

### IF: 

```abap

   IF time < '120000'.
    comportamento desejado
   ELSEIF time > '120000'.
    comportamento desejado
   ELSE.
    comportamento desejado
   ENDIF. 
```

&-------------------------------------------------&

### DO:
```abap
    DO 5 TIMES.
        comportamento desejado
    ENDDO.    
```
&-------------------------------------------------&

### WHILE:
```abap
    WHILE l_int < 5.
         comportamento desejado
    ENDWHILE.
```
&-------------------------------------------------&

### LOOP:

    No SAP costumamos trabalhar com tabelas em tempo de execução (Tabelas Internas) e linhas da tabela (Work Area).
    Para conseguir os dados da tabela nós usamos o LOOP AT.

    it_e070    -> Tabela interna
    wa_e070 -> Linha da tabela
```abap
    LOOP AT it_e070 INTO wa_e070.
        comportamento desejado
    ENDLOOP.
```
&-------------------------------------------------&






## Operadores Aritméticos

(+) – adição.
(-) – subtração.
(*) – multiplicação.
(/) – divisão.
DIV – divisão inteira.
MOD – Resto da divisão inteira.
** – Potenciação.

Ao usar expressões matemáticas, os operadores +, -, *, **, e /, bem como abertura e fechamento de parênteses, são interpretados como palavras ABAP e devem ser precedidos e seguidos por espaços em branco.

Em operações de divisão, o divisor não pode ser zero se o dividendo não é zero. Com a divisão inteira, você usa os operadores DIV ou MOD em vez de /. DIV calcula o quociente inteiro, MOD calcula o resto da divisão.


##### Fontes

http://descomplicaabap.blogspot.com/2015/11/estruturas-de-condicoes-e-loops-abap.html
