# Capítulo 9

## Testes de unidade

### As três leis do TDD:

#### *Primeira lei:*

Não se deve escrever o código de produção até criar um teste de unidade de falhas;

#### *Segunda lei:*

 Não se deve escrever mais de um teste de unidade do que o necessário para falhar, e não compilar é falhar;

#### *Terceira lei:*

 Não se deve escrever mais códigos de produção do que o necessário para aplicar o teste de falha atual.

Os testes e o código de produção são escritos juntos, com os testes apenas alguns segundos adiantados.

Trabalhando assim, criaríamos dezenas de testes a cada dia, centenas a cada mês e milhares a cada ano. Os testes cobririam praticamente todo o nosso código de produção, mas o tamanho completo desses testes pode apresentar um problema de gerenciamento.

### Como manter os testes limpos

Muitos testes devem ser alterados conforme o código de produção evolui, se sua equipe não gosta ou acha testes uma perca de tempo e produtividade, ruim com eles? Muito pior sem eles. É como um avalanche que começa pequeno e no final está gigante destruindo tudo pela frente. Hoje é uma funcionalidade que não é testada, amanhã uma alteração em código legado, depois está um amaranhado que não se sabe onde começar a alterar no código. No final o código de produção começa a se degradar, e o resultado é um código sem testes, confuso e cheio de bugs, com consumidores frustrados e o projeto inacabado e sem uso. Testes limpos é o início de um caminho tranquilo para a qualidade.

A moral é que os códigos de testes são tão importantes quanto o código de produção, ele não é um componente secundário, ele requer raciocínio, planejamento e cuidado, é preciso mantê-lo tão limpo quanto o código de produção.

São os códigos de testes que mantêm os códigos flexíveis, reutilizáveis e passíveis de manutenção. Isso porque se você tiver testes, não terá medo de alterar o código, sem os testes, cada alteração pode gerar um bug. Não importa o grau de flexibilidade de sua arquitetura ou de divisão de seu modelo, sem os testes você ficará relutante em fazer mudanças. Mas quanto maior a cobertura de seus testes, menor o medo.

O que define testes limpos? LEGIBILIDADE! O que torna os testes legíveis? O mesmo que torna todo código legível: CLAREZA, SIMPLICIDADE e CONSISTÊNCIA DE EXPRESSÃO.

Há uma escola de pensamento que diz que cada função de teste deve ter um e apenas uma instrução de confirmação (assert), além de defender um único conceito em cada função de teste.

### *F.I.R.S.T*

Testes limpos seguem outras cinco regras que forma o acrônimo em inglês FIRST, que signfica (Fast, Independet, Repeatable, Self-validating, Timely):

#### *Rapidez:*
 Testes devem ser rápidos

#### *Independência:*
 Os testes não devem depender uns dos outros

#### *Repetitividade:*
 Deve-se poder repetir os testes em qualquer ambiente.

#### *Autovalidação:*
 Os testes devem ter uma saída booleana, obtenham ou não êxito.

#### *Pontualidade:*
 Os testes precisam ser escritos em tempo hábil, imediatamente antes do código de produção no qual serão aplicados.

Aqui abordamos apenas o nício deste tópico. De fato, acho que deveria ter um livro interiro sobre Testes limpos. Os testes são tão importantes para a saúde de um projeto quando o código de produção. Talvez até mais, pois eles preservam e aumentam a flexibilidade, capacidade de manutenção e reutilização do código de produção. Portanto, mantenha seus testes sempre limpos. Trabalhe para torna-los sucintos e expressivos. Investe APIS de teste que funcione como uma linguagem especifica a um dominio que lhe ajude a criar seus testes. Se deixar os testes de degradarem, seu código também irá. Mantenha limpos os seus testes.

