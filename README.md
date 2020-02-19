# Abap

## Estruturas de condições e Loops SAP

#### IF: 

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

#### DO:
```abap
    DO 5 TIMES.
        comportamento desejado
    ENDDO.    
```
&-------------------------------------------------&

#### WHILE:
```abap
    WHILE l_int < 5.
         comportamento desejado
    ENDWHILE.
```
&-------------------------------------------------&

#### LOOP:

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

(+) – adição.<br>
(-) – subtração.<br>
(*) – multiplicação.<br>
(/) – divisão.<br>
DIV – quociente da divisão inteira.<br>
MOD – resto da divisão inteira.<br>
** – potenciação.<br>

Ao usar expressões matemáticas, os operadores +, -, *, **, e /, bem como abertura e fechamento de parênteses, são interpretados como palavras ABAP e devem ser precedidos e seguidos por espaços em branco.<br>

Em operações de divisão, o divisor não pode ser zero se o dividendo não é zero.<br>


##### Fontes

http://descomplicaabap.blogspot.com/2015/11/estruturas-de-condicoes-e-loops-abap.html

https://desenvolvimentoaberto.org/2014/02/15/looping-while-e-expressoes-aritmeticas-abap/
