# Onde estamos pisando

Antes de tudo, vamos tentar entender o terreno espinhoso pelo qual estamos nos aventurando. Uma rápida visão geral pode ser útil para nos sentirmos menos perdidos no meio do caminho.

Na internet, surgiu a relação conhecida como Cliente-Servidor. Nesse contexto, a palavra “servidor” denomina o computador, ou o programa, que fornece um serviço a um “cliente”, o qual pode, da mesma forma, ser um computador ou programa.

Apesar de ser um conceito intrinsecamente ligado à conectividade da internet, a verdade é que esses dois elementos podem coexistir dentro de uma mesma máquina e dispensar completamente qualquer ligação com o mundo exterior. Essa é uma situação incomum no dia a dia de um usuário de computador, mas, dependendo da sua experiência com RAC, você pode tê-la vivido sem perceber.

Ferramentas como o [OpenRefine](http://openrefine.org/) (antigo Google Refine), usado para acelerar a busca por inconsistências em bancos de dados, podem ser utilizados pelo seu navegador (ex. Internet Explorer, Firefox, Chrome) e têm a aparência de um site comum da internet, mas não estão hospedados em um servidor distante. Na verdade, o Refine foi construído para ter seu código executado dentro do próprio computador de quem o usa. Dessa forma, quando você faz o “upload” de uma tabela para ele, na verdade está apenas passando as informações de um programa para outro dentro da sua máquina. Isso é bom, porque dispensa você de compartilhar o conteúdo, potencialmente sigiloso, com terceiros.

MySQL é normalmente executado em computadores remotos, mas para desenvolvermos nosso trabalho com mais segurança e estabilidade, trabalharemos sempre dentro de nossos próprios computadores.

# Prepare suas ferramentas

O trabalho deste manual envolverá duas ferramentas livres e gratuitas, disponíveis para todos na internet: [Xampp](https://www.apachefriends.org/pt_br/download.html) e [HeidiSQL](http://www.heidisql.com/download.php). Mesmo sendo de código aberto, o suporte de ambas ao português é pobre e, portanto, vamos nos ater a suas edições em inglês.

Ambas são compatíveis com Windows, que é o foco deste manual. Usuários de Mac OS vão precisar usar o [Sequel Pro](http://www.sequelpro.com/download/) como alternativa ao HeidiSQL. As interfaces são um pouco diferentes, mas o uso da linguagem SQL não difere em nada.

Configurar um servidor MySQL pode envolver algumas etapas desnecessariamente complexas para o que queremos construir com nosso trabalho, e por isso vamos usar o pacote de servidores pré-configurado Xampp para nos pouparmos disso.

Poderíamos lidar com nosso servidor de banco de dados apenas com comandos de texto, tanto para ver como para controlar nossas informações. No entanto, usaremos interfaces gráficas como HeidiSQL para eliminar gasto de tempo desnecessário para nossos objetivos e focarmos o aprendizado em relacionamentos mais complexos de tabelas.

Baixe os aplicativos e instale-os. Vale observar que, mesmo sem ter permissões de administrador, situação comum em computadores de redações, é possível usar essas ferramentas sem qualquer prejuízo no Windows. Apenas procure pelas versões “portable” nas páginas de download.
