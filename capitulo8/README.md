# Capítulo 8

## Limites de códigos de terceiros

De vez em quando precisamos de pacotes de outros fabricantes ou usamos códigos livres, de algum modo, precisamos integrar de forma limpa código externo ao nosso, este capítulo se preocupa em mostrar práticas e técnicas para manter limpos os limites de nosso software.

Passar adiante código de terceiros por todo o seu projeto significa dizer que em caso de mudança, manutenção ou alteração de pacote, haverá vários lugares para mexer.

Códigos de terceiros nos ajudam a obter mais funcionalidades em menos tempo, não é tarefa nossa testá-lo, mas pode ser melhor para nós criar testes para os códigos externos que fomos usar. Antes de decidir usar código de terceiro, é interessante testar antes sua implementação, para não precisar de sessões de depuração tentando descobrir se os bugs encontrados são do nosso código ou do pacote externo.

Entender e integrar código de terceiro é difícil, fazer ambos ao mesmo tempo dobra a dificuldade, uma alternativa de abordagem a experimentação é exatamente criar testes para explorar nosso conhecimento sobre ele. Jim Newkirk chama isso de testes de aprendizagem.

Nesse momento ele fala sobre o *_log4j_*, e quem é da área lembra do caos que teve com uma atualização recente desse pacote, é um exemplo prático de limite e testes de código de terceiro.

Os testes de aprendizagem são experimentos precisos que ajudam a aumentar nosso entendimento, esses testes não só saem de graça como geram um retorno positivo de nosso investimento. Quando houver novas distribuições daquele pacote externo, podemos executar os testes para ver se há diferenças nas atividades, porque uma vez integrados, não há garantias de que o código se manterá compatível com as nossas necessidades.

Cada distribuição vem com um novo risco, se as alterações invalidem nossos testes, descobriremos de imediato.

O código precisa de uma divisão clara e testes que definem o que se deve esperar, evitando que grande parte de nosso código enxergue as particularidades dos de terceiros, é melhor depender de algo que você controle do que pegar algo que acabe controlando você.

Nesse capítulo, a forma como é tratado o uso de códigos de terceiros, é um convite a conhecer mais sobre testes automatizados, princípios SOLID e Domain Driven Design, assuntos que tenho interesse em me aprofundar.


