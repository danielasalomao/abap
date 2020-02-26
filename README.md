# Abap
---
## Tipos de Dados Padrão ABAP

i –  integer 4 byte número inteiro + / – 2,1 bilhões<BR>
f –  floar 8 bytes, 15-16 dígitos significativos<BR>
c – string de até 65 mil caracteres<BR>
n – numeric string até 65 mil caracteres (número não-matemático)<BR>
string – de comprimento dinâmico até 2 GB de comprimento!<BR>
xstring –  hex string seqüêncial de byte comprimento de dinâmico<BR>
x –  byte seqüêncial de até 65k bytes<BR>
d –  Data 8 caracteres de formato AAAAMMDD<BR>
t –  tempo 6 caracteres de HHMMSS<BR>
p  – packed number preciso ou número flutuante de até 16 bytes<BR>
   
![Alt Text](https://github.com/danielasalomao/abap/blob/master/data-types.jpg)

---
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





---
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


---

## Criar Transação

SE93



---

## Transações

* **SE01**: Criar request
* **SE09**: Liberar request
* **SE10**: Olhar request
* **SE11**: ...
* **SE38**: ...
* **BAPI**: ...



---

## Pacote

* **ZEXODO**: Todos os desenvolvimentos, seja transação ou códigos que solicitarem pacotes, devem ser incluídos no pacote ZEXODO






---

## DEV100 PARA DEV150

O código de transação **SCC1** é usado para transportar a solicitação de um cliente diferente no mesmo sistema, exemplo você deseja transportar a solicitação xxxx do cliente 100 para o cliente 150 no sistema DEV.

##### Fontes :ledger:

http://descomplicaabap.blogspot.com/2015/11/estruturas-de-condicoes-e-loops-abap.html

https://desenvolvimentoaberto.org/2014/02/15/looping-while-e-expressoes-aritmeticas-abap/



---

##### Emoji do GitHub

[EMOJI CHEAT SHEET](https://www.webfx.com/tools/emoji-cheat-sheet/)

[All-Github-Emoji-Icons](https://github.com/scotch-io/All-Github-Emoji-Icons)
