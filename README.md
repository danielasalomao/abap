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

## Tipos de Tabelas

#### Internal Table
* **Standard Table**: ...
* **Sorted Table**: ...
* **Hashed Table**: ...

#### Transparent Table 

* **Informações**: Funcionamento é idêntico a qualquer outra tabela de um banco de dados relacional.Para cada Transparent Table definida na SE11 (Data Dictionary) uma tabela física é criada no banco de dados com exatamente o mesmo nome, os mesmos campos e os mesmos índices.

#### Pooled Table
#### Cluster Table





---
## Tabelas X Estruturas

   - Dados podem ser armazenados fisicamente na Tabela, na Estrutura não pode.<br>
   - Estrutura não tem chave primária, tabela pode ter. <br>
   - Tabela pode ter o atributo técnico, estrutura não tem.


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



---

## ALV

Três formas diferentes de visualização: lista simples, lista sequencial hierarquizada ou uma arvore. 

### ALV de lista simples

 - Estrutura dividida em duas dimensões simples: estrutura de título e outra de dados, de forma direta. 
 - Os dados devem ter a mesma estrutura e listarem os registros um abaixo do outro.
 - 90% dos relatórios.
 - Estrutura formada por colunas.
 - Principal função para criar: REUSE_ALV_LIST_DISPLAY
 - Outras funções que podem ser utilizadas na criação de um ALV simples
 
      Reuse_alv_fieldcatalog_merge (Função para montar o Field Catalog essencial para configurar os dados da saída);<br>
      Reuse_alv_list_display (Função de apresentação dos dados);<br>
      Reuse_alv_events_get (Função para criar eventos na lista de saída);<br>
      Reuse_alv_grid_display (Apresenta o resultado num grid full screen);<br>
      Reuse_alv_commentary_write (Criar um cabeçalho com informações desejadas);<br>

### ALV Sequencial hierarquizada

 - Estrutura em formato de árvore.
 - Mostra os tipos de dados em níveis de hierarquia.
 - Principal função para criar: REUSE_ALV_HIERSEQ_LIST_DISPLAY
 - Outr função muito utilizada: REUSE_ALV_FIELDCATALOG_MERGE


### ALV Tree

 - Principal função para criar: RS_TREE_LIST_DISPLAY
 

### Outras formas de apresentação de um ALV:

#### ALV Grid Control
   - Exige a criação de uma tela no report ou module-pool
   - Definição de uma área de container para apresentação do resultado
   - Classes principais: CL_GUI_ALV_GRID ou CL_SALV_TABLE

#### ALV Hierarchical sequential control
   - Exige a criação de uma tela no report
   - Classe: CL_SALV_HIERSEQ_TABLE ou Função: REUSE_ALV_HIERSEQ_LIST_DISPLAY

#### ALV Grid Full Screen
   - Principal função para criar: REUSE_ALV_GRID_DISPLAY
   - Semelhante a lista simples

#### ALV Tree Controle
   - Orientado a Objeto
   - Classes principais: CL_GUI_ALV_TREE e CL_SALV_TREE

#### ALV WebDynpro



## Programas que SAP disponibiliza como exemplo para ajudar desenvolvedores ABAP:
   - BCALV_TEST_FULLSCREEN
   - BCALV_TEST_FULLSCREEN
   - BCALV_TEST_FULLSCREEN_EDIT
   - BCALV_TEST_FULLSCREEN_EVENTS
   - BCALV_TEST_FULLSCREEN_FILTER
   - BCALV_TEST_FULLSCREEN_FQUAN
   - BCALV_TEST_FULLSCREEN_HTML
   - BCALV_TEST_FULLSCREEN_PRINT
   - BCALV_TEST_FULLSCREEN_STATUS


---

##### Fontes :ledger:

http://descomplicaabap.blogspot.com/2015/11/estruturas-de-condicoes-e-loops-abap.html

https://desenvolvimentoaberto.org/2014/02/15/looping-while-e-expressoes-aritmeticas-abap/

https://goenning.net/2015/03/13/os-diferentes-tipos-de-tabela-do-sap/

http://sapguru99.com/top-35-de-perguntas-e-respostas-da-entrevista-sap-abap/

http://sapguru99.com/tutorial-do-dicionario-de-dados-abap-se11-tabela-objeto-de-bloqueio-visualizacao-e-estrutura/

https://qametrik.com/domine-a-construcao-de-alv/

---

##### Emoji do GitHub

[EMOJI CHEAT SHEET](https://www.webfx.com/tools/emoji-cheat-sheet/)

[All-Github-Emoji-Icons](https://github.com/scotch-io/All-Github-Emoji-Icons)
