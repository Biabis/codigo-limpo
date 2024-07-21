## Exemplo Correto

```java
public class UsuarioService {
    
    public Usuario buscarUsuarioPorId(int id) {
        try {
            return buscarUsuarioNoBanco(id);
        } catch (SQLException e) {
            throw new RuntimeException("Erro ao buscar usuário", e);
        }
    }

    private Usuario buscarUsuarioNoBanco(int id) throws SQLException {
        // Simulação de busca no banco de dados
        // Código de busca no banco de dados
    }

    public void atualizarEmailUsuario(int id, String novoEmail) {
        validarEmail(novoEmail);
        try {
            atualizarEmailNoBanco(id, novoEmail);
        } catch (SQLException e) {
            throw new RuntimeException("Erro ao atualizar email do usuário", e);
        }
    }

    private void atualizarEmailNoBanco(int id, String novoEmail) throws SQLException {
        // Simulação de atualização no banco de dados
        // Código de atualização no banco de dados
    }

    private void validarEmail(String email) {
        if (email == null || !email.contains("@")) {
            throw new IllegalArgumentException("Email inválido");
        }
    }
}
```
## Exemplo Incorreto

```java

public class UsuarioService {
    
    public Usuario buscarUsuario(int id) {
        Usuario usuario = null;
        try {
            // Simulação de busca no banco de dados
            // Código de busca no banco de dados
        } catch (SQLException e) {
            System.err.println("Erro ao buscar usuário: " + e.getMessage());
            return null;
        }
        return usuario;
    }

    public boolean atualizarEmailUsuario(int id, String novoEmail) {
        if (novoEmail == null || !novoEmail.contains("@")) {
            return false; // Código de erro
        }
        try {
            // Simulação de atualização no banco de dados
            // Código de atualização no banco de dados
        } catch (SQLException e) {
            System.err.println("Erro ao atualizar email do usuário: " + e.getMessage());
            return false; // Código de erro
        }
        return true;
    }
}
```

## Explicação das Diferenças

### Funções Pequenas e de Único Propósito:

#### *Correto:* 

As funções buscarUsuarioPorId e atualizarEmailUsuario são pequenas e fazem uma única coisa. Funções auxiliares como buscarUsuarioNoBanco, atualizarEmailNoBanco, e validarEmail são extraídas para manter o código limpo e seguindo o SRP.

#### *Incorreto:*

 As funções buscarUsuario e atualizarEmailUsuario são grandes e fazem várias coisas ao mesmo tempo, como validação, busca/atualização no banco e tratamento de erros.

### Nível de Abstração:

#### *Correto:* 

 Cada função está no mesmo nível de abstração e é clara em seu propósito.

#### *Incorreto:*

 A função atualizarEmailUsuario tem múltiplos níveis de abstração, misturando validação, atualização e tratamento de erros.

### Nomes Descritivos:

#### *Correto:* 

  Os nomes das funções e variáveis são descritivos, como buscarUsuarioPorId e atualizarEmailNoBanco.

#### *Incorreto:*

 Os nomes são menos descritivos e não deixam claro o propósito das funções.

### Parâmetros de Funções:

#### *Correto:* 

 As funções utilizam no máximo dois parâmetros (atualizarEmailUsuario).

#### *Incorreto:*

 A quantidade de parâmetros é aceitável, mas a complexidade das funções não é reduzida, tornando a leitura difícil.

### Parâmetros Lógicos:

#### *Correto:* 

 Não utiliza parâmetros lógicos.

#### *Incorreto:*

Também não utiliza parâmetros lógicos, mas há falhas em outros princípios.

### Evitar Efeitos Colaterais:

#### *Correto:* 

 As funções não têm efeitos colaterais inesperados.

#### *Incorreto:*
 As funções possuem efeitos colaterais, como a impressão de mensagens de erro diretamente.

### Exceções vs. Código de Erro:

#### *Correto:* 

 Utiliza exceções para tratamento de erros, o que é mais claro e separado da lógica principal.

#### *Incorreto:*

Utiliza código de erro (return false), o que pode levar a problemas de legibilidade e manutenção.

### Extração de Blocos Try/Catch:

#### *Correto:* 

 Os blocos try/catch são extraídos para funções específicas, mantendo o SRP.

#### *Incorreto:*

 O tratamento de exceções está diretamente nas funções principais, quebrando o SRP.

### Evitar Repetição:

#### *Correto:* 
 Não há repetição de código.

#### *Incorreto:*

 Não há muita repetição, mas a falta de separação clara de responsabilidades aumenta a complexidade.


Esses exemplos demonstram como seguir esses princípios pode levar a um código mais limpo, legível e fácil de manter.
