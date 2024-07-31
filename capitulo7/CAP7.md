# Capítulo 7

## Tratamento de erros

Sistemas irão falhar, usuários irão fornecer entradas erradas, o hardware pode falhar, as coisas podem dar errado e quando isso acontece, nós somos os responsáveis por certificar que nosso código faça o que for preciso. O tratamento de erro domina completamente muitos código-fonte, é um recurso fundamental em um software, o autor trás algumas técnicas para lidar com erros com elegância e estilo. Para isso podemos realizar a verificar de alguns tópicos: 

- Use exceções em vez de retornar códigos

- Crie primeiro sua estrutura try-catch-finally

- Use exceções não verificadas

- Forneça exceções com contexto

- Defina as classes de exceções segundo as necessidades do chamador, empacotar APIs de terceiros é a melhor prática que existe, dessa forma você minimiza as dependências nelas, você pode escolher migrar para uma biblioteca diferente no futuro sem muitos problemas. E também facilita a simulação de chamadas de terceiros quando for testar seu próprio código.

- Defina o fluxo normal

- Não retorne null, você precisará checar o retorno se é null ou false em todas validações

- Não passe null para os métodos, seguindo a linha de pensamento de não retornar null

Uma código limpo é legível, mas também precisa ser robusto. Esses objetivos não são conflitantes. POdemos criar programas limpos e robustos se enxergarmos o tratamento de erro como uma preocupação à parte, algo que seja visível independentemente de nossa lógica principal. Na medida em que somos capazes de fazer isso, podemos pensar nisso de forma independente e dar um grande passo na capacidade de manutenção de nosso código.

