# Capítulo 6

## Objetos e Estrutura de dados

O primeiro questionamento feito nesse capítulo é por que tantos programadores adicionam métodos de acesso (escrita e leitura) em objetos e variáveis que são, ou deveriam ser, privadas? Ele continua exemplificando as diferentes formas de alterar funcionalidades de classes, seja adicionando tipos de dados ou adicionando funções. Afirma que haverá vezes nas quais desejaremos adicionar novos tipos de dados em vez de novas funções, e que nesses casos, objetos e OO são mais apropriados. Por outro lado, também haverá vezes que desejaremos adicionar novas funções em vez de tipos de dados, neste caso, estrutura de dados e código procedimental são mais adequados.

### A lei de Demeter
Um módulo não deve enxergar o interior dos objetos que ele manipula, os objetos escondem seus dados e expõem as operações, o que significa dizer que um objeto não deve expor sua estrutura interna por meio dos métodos acessores, pois isso seria expor sua estrutura interna. Em outras palavras, fale apenas com conhecidos e não com estranhos.

Carrinho de trem, esse tipo de código costuma ser chamado de carrinho de trem, pois parece um monte de vagões acoplados. Cadeias de chamadas como essa geralmente são consideradas descuidadas e devem ser evitadas.

### Híbridos
Essa confusão leva a estruturas híbridas ruins que são metade objeto e metade estrutura de dados. Elas possuem funções que fazem algo significativo e também variáveis ou métodos de acesso e de alteração públicos de variáveis privadas. Evite criá-los.

Em suma, os objetos expõem as ações e ocultam os dados, facilitando adição de novos tipos de objetos sem precisar modificar as ações existentes e dificulta a inclusão de novas atividades em objetos existentes. As estruturas de dados expõem os dados e não possuam ações significativas, facilitando a adição de novas ações às estruturas de dados existentes e dificultando a inclusão de novas estruturas de dados em funções existentes. Terá momentos que desejaremos flexibilidade para adicionar novos tipos de dados e optaremos por objetos, em outras ocasiões, desejaremos flexibilidade para adicionar novas funções, e portanto, optaremos por tipos de dados e procedimentos. Cabe a nós entender essas questões sem preconceito e selecionar a abordagem que melhor se aplica no momento.



