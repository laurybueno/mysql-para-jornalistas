# Guia rápido para SQL orientado a investigação de dados

Apenas para fins de consulta, aqui você tem reunidas as principais ferramentas da linguagem SQL apresentadas neste manual:

*WHERE – define filtros para seus resultados*
```sql
SELECT votos, can_id FROM tb_eleicoes_10_dados WHERE can_id = 0
```

*LIKE – permite comparar valores incompletos como partes de números ou palavras*
```sql
SELECT * FROM tb_formato_valor WHERE fmt_cod LIKE '%40%'
```

*!= – significa “diferente”*
```sql
SELECT votos, can_id, tipo, tipo2 FROM tb_eleicoes_10_dados WHERE tipo != tipo2
```

*GROUP BY – agrupa os resultados de acordo com um campo escolhido. Pode ser combinado com as funções SUM e COUNT*
```sql
SELECT ano, inst, COUNT(inst) FROM candidatos WHERE (ano = '2010' and turno = '1') GROUP BY inst
```

*SUM – soma os valores de um campo em todas as linhas selecionadas. É frequentemente usado com GROUP BY*
```sql
SELECT SUM(votos), cargo FROM tb_eleicoes_10_dados WHERE (tipo = '4' or tipo = '3') and turno = '1' GROUP BY cargo
```

*COUNT – conta o número de vezes em que determinado campo aparece nos dados resultantes da query, independentemente dos valores contidos. Assim como o SUM, ele ganha eficácia com GROUP BY*
```sql
SELECT ano, inst, COUNT(inst) FROM candidatos WHERE (ano = '2010' and turno = '1') GROUP BY inst
```

*LIMIT – limita o número de linhas que pode ser retornado por uma query. Serve para evitar sobrecarga em casos de querys com muitos resultados ou muito complexas, como JOIN*
```sql
SELECT * FROM candidatos WHERE ano = '2010' and turno = '1' LIMIT 100
```

*RIGHT JOIN / LEFT JOIN – emenda tabelas baseado em uma condição determinada após a expressão ON. Pode ser repetido dentro de uma mesma query para unir mais de duas tabelas*
```sql
SELECT candidatos.*, tb_eleicoes_10_dados.votos FROM tb_eleicoes_10_dados RIGHT JOIN candidatos ON candidatos.can_id = tb_eleicoes_10_dados.can_id  WHERE candidatos.ano = '2010' and tb_eleicoes_10_dados.votos != 'NULL' LIMIT 100
```
