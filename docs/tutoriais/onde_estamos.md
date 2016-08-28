# Onde estamos pisando

Antes de tudo, vamos tentar entender o terreno espinhoso pelo qual estamos nos aventurando. Uma rápida visão geral pode ser útil para nos sentirmos menos perdidos no meio do caminho.

Na internet, surgiu a relação conhecida como Cliente-Servidor. Nesse contexto, a palavra “servidor” denomina o computador, ou o programa, que fornece um serviço a um “cliente”, o qual pode, da mesma forma, ser um computador ou programa.

Apesar de ser um conceito intrinsecamente ligado à conectividade da internet, a verdade é que esses dois elementos podem coexistir dentro de uma mesma máquina e dispensar completamente qualquer ligação com o mundo exterior. Essa é uma situação incomum no dia a dia de um usuário de computador, mas, dependendo da sua experiência com RAC, você pode tê-la vivido sem perceber.

Ferramentas como o [OpenRefine](http://openrefine.org/) (antigo Google Refine), usado para acelerar a busca por inconsistências em bancos de dados, podem ser utilizados pelo seu navegador (ex. Internet Explorer, Firefox, Chrome) e têm a aparência de um site comum da internet, mas não estão hospedados em um servidor distante. Na verdade, o Refine foi construído para ter seu código executado dentro do próprio computador de quem o usa. Dessa forma, quando você faz o “upload” de uma tabela para ele, na verdade está apenas passando as informações de um programa para outro dentro da sua máquina. Isso é bom, porque dispensa você de compartilhar o conteúdo, potencialmente sigiloso, com terceiros.

MySQL é normalmente executado em computadores remotos, mas para desenvolvermos nosso trabalho com mais segurança e estabilidade, trabalharemos sempre dentro de nossos próprios computadores.
