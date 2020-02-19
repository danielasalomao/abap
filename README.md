# Abap

## Estruturas de condições e Loops SAP

### IF:

   IF time < '120000'.<br>
    comportamento desejado<br>
   ELSEIF time > '120000'.<br>
    comportamento desejado<br>
   ELSE.<br>
    comportamento desejado<br>
   ENDIF. <br>

&-------------------------------------------------&

### DO:

    DO 5 TIMES.
        comportamento desejado
    ENDDO.    

&-------------------------------------------------&

### WHILE:

    WHILE l_int < 5.
         comportamento desejado
    ENDWHILE.

&-------------------------------------------------&

### LOOP:

    No SAP costumamos trabalhar com tabelas em tempo de execução (Tabelas Internas) e linhas da tabela (Work Area).
    Para conseguir os dados da tabela nós usamos o LOOP AT.

    it_e070    -> Tabela interna
    wa_e070 -> Linha da tabela

    LOOP AT it_e070 INTO wa_e070.
        comportamento desejado
    ENDLOOP.

&-------------------------------------------------&









##### Fontes

http://descomplicaabap.blogspot.com/2015/11/estruturas-de-condicoes-e-loops-abap.html
