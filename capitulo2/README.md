# Capítulo 2

Já no capítulo 2, o autor vai abordar a importancia de nomes significativos e que demosntrem seu significado.

Pra que um nome seja ele de função, classe, variável ou objeto siga o padrão indicado o mesmo deve respeitar alguns tópicos, são eles: 

- Use nome que revelem o propósito;
- Não passe informações erradas;
- Utilize nomes que possam ser fáceis de diferencia-los para não haver confusão;
- Use nomes pronunciáveis;
- Use nomes que possam ser posteriormente pesquisados;
- Evite nomes codificados;
- Adicione um contexto que dê significado;


#### É importante resaltar: 

- Nome de classes e objetos com substantivos;

- Nome de métodos/funções com verbo;


Nomear coisas é realmente um trabalho chatinho às vezes e nem sempre dar certo de primeira. Para quem está iniciando, é interessante perder um tempinho procurando métodos de renomear arquivos, classes, funções e variáveis dinamicamente na sua IDE. Te salva um tempão e te ajuda a melhorar a qualidade no seu código, o que é muito avaliado inicialmente. Nomes não é uma coisinha tão simples de se fazer em programação e que te vale muito. Não negligencie.


```java
 public class MausExemplosDoCapitulo2 {
    // Pode-se reparar que ao ler essa variável dificilmente saberemos do que ela se trata, há esforço significativo para tentar entendê-la
    private int d;

    // Aqui podemos reparar que essa função pode se tratar de qualquer coisa, não há nada que dê significado a ela.
    public List<int[]> getThem() {
        List<int[]> list1 = new ArrayList<int[]>();

        for(int[] x : theList)
            if (x[0] == 4) {
                list1.add(x);
            }
        return list1;
    }



    // Veja que essas duas variáveis tem nomes bastantes parecidos, sendo difícil de diferenciá-los.
    private produtoMarcadoEmEstoqueForaDaValidadeComDesconto;
    private produtoMarcadoEmEstoqueDentroDaValidadeComDesconto;

    public static void copyChars(char a1[], char a2[]) {
        for (int i = 0; i < a1.length; i++) {
            a2[i] = a1[i];
        }
    }
}

// Pode-se verificar que caso não tivesse o pré-fixo address nos atributos o significado dos mesmos seriam confudidos, adicionando
// um nome significativo à classe excluiriamos esse pré-fixo assim economizando caracteres e mantendo a boa leitura da classe.
public class User {
    private String addressName;
    private String addressZipCode;
    private String addressCity;
}
```




