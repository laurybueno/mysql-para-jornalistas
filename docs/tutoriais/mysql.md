# Hierarquia de dados

Dentro de seu servidor MySQL, podem ser criados tantos bancos de dados quantos forem necessários, da mesma forma que se pode indefinidamente criar arquivos para usar no Microsoft Excel.

Dentro de cada banco, você pode criar tabelas. Analogamente, pense nas planilhas que podem ser criadas dentro de cada arquivo do Excel.

Apesar dessas semelhanças, MySQL guarda várias complexidades que podem tanto nos ajudar quanto nos atrapalhar em nossos processos. Ao criar tabelas, por exemplo, é necessário determinar com antecedência quais tipos de dados cada campo conterá.

# Sintaxe

Apesar de o HeidiSQL nos entregar uma interface gráfica para falarmos com nossos bancos de dados, nós vamos precisar aprender a escrever comandos em texto para aproveitarmos todo o potencial do sistema.

As requisições para o servidor são chamadas de “querys” e têm, basicamente, três partes:

```plain
<comando a ser executado> <tabela afetada> <dados filtrados>
```

O comando principal será quase sempre “SELECT”. As tabelas afetadas serão as que construiremos com nossos dados. E, por fim, esses dados serão especificados com a ajuda de cláusulas como a “WHERE”.

```sql
SELECT custo FROM investimentos WHERE gestao = "kassab"
```

No exemplo acima, são processados os conteúdos de uma tabela criada previamente e chamada “investimentos”. Nela, entre outras colunas, temos “custo” e “gestao”. Neste caso, vamos pressupor que já existam linhas nessa tabela e que essas linhas tenham as duas colunas preenchidas.

O objetivo da query, explicitado logo na primeira palavra, é selecionar (entenda exibir na tela) o conteúdo da coluna “custo”, e apenas dela, de dentro (“FROM”) da tabela “investimentos”. Sendo que apenas (“WHERE”) a gestão “kasab” nos interessa.

Quando você quiser selecionar todas as colunas de uma mesma tabela, pode usar um asterisco em vez de escrever todos os nomes após o “SELECT”.
