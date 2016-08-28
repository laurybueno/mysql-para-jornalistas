# HeidiSQL

Esse software é apenas uma das muitas possibilidades de interfaces gráficas para MySQL. Você pode usar a que lhe convier. Escolhemos o [HeidiSQL](http://www.heidisql.com/download.php) para este manual por lidar mais rapidamente com grandes carregamentos de dados; situação essa que deveremos enfrentar diversas vezes com informações brutas fornecidas por governos. Mais adiante, teremos que cruzar uma tabela de quase 600 mil linhas com outras não muito menores. Essa quantidade de dados representa grande esforço não só para o próprio MySQL, como também para a interface gráfica que escolhemos.

Outra ferramenta também bastante robusta é o phpMyAdmin, que faz parte do pacote Xampp e pode ser encontrado no menu à esquerda do site [http://localhost/](http://localhost/). Lembre-se apenas que, para usá-lo, são necessários tanto o servidor MySQL quanto o Apache rodando em seu computador. Se não está claro para você como fazer isso, [leia este guia sobre Xampp](xampp.md).

![Screeshot](../img/heidisql-inicio.png)

Para começarmos, devemos configurar o acesso do programa para nosso servidor local. Clique em “New”.

![Screeshot](../img/heidisql-nova-comexao.png)

Mude o nome da sessão que estamos criando de “Unnamed” para “RAC - Servidor”, ou outro nome que preferir. No campo “password”, escreva a senha que escolheu para seu usuário “root” após a instalação do Xampp. Clique em “Save” e em “Open”.

A partir de agora, você deve ficar atento às diferenças entre letras maiúsculas e minúsculas que usar em tudo que escrever. Para nomes de bancos de dados, por exemplo, “Rac” é diferente de “rac” que é diferente de “RAC”.

Agora, deve-se abrir para você a janela principal do HeidiSQL. Ela servirá a quase todos os nossos trabalhos de Reportagem com o Auxílio do Computador. Mas, primeiro, vamos criar um banco de dados para mantermos nossos exercícios separados de outras informações que você poderá inserir nesse sistema no futuro.

![Screeshot](../img/heidsql-servidor-aberto.png)

Na coluna à esquerda, clique com o botão direito do mouse sobre “RAC - Servidor”. As opções que vão aparecer se referem ao seu servidor local de banco de dados. Neste momento, queremos criar um banco novo. Escolha “Create New” -> ”Database”.

Chame o banco de dados de “rac”, em “Character set” escolha “latin1” e em “Collation” selecione “latin1_general_ci”. Essa configuração deve dar conta da maior parte dos bancos de dados em português que você poderá encontrar de fontes brasileiras. Essa informação diz respeito a caracteres especiais que poderemos inserir no sistema. Letras com acentos, por exemplo, podem ser afetadas se você fizer a escolha errada neste momento. Apesar de importante, ela sempre pode ser modificada no futuro.

Se essa não for a combinação correta, você também pode tentar o muito utilizado “utf8” com “utf8_general_ci”.

Repare que, nessa mesma janela, há alguns comandos em formato de texto logo abaixo. Se você continuar mexendo nas configurações, verá que eles mudam de acordo. Isso ajuda a esclarecer o verdadeiro papel do HeidiSQL em nosso trabalho. Ele escreve comandos chatos no nosso lugar. Ou seja, faz com mais agilidade coisas corriqueiras como criar bancos, tabelas ou ler resultados simples.

Mas, é importante lembrar que para tirar proveito da flexibilidade que esse ambiente proporciona, é preciso entender muito bem essa linguagem. Portanto, não a ignore.
