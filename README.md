<h1>Projeto Loja de Games</h1>

## Diagrama de Classes

```mermaid
classDiagram
class Categoria {
  - id : Long
  - tipo : String
  - produto : List ~Produto~
  + getAll()
  + getById(Long id)
  + getByTipo(String tipo)
  + post(Categoria categoria)
  + put(Categoria categoria)
  + delete(Long id)
}
class Produto {
  - id : Long
  - nome : String
  - descricao: String
  - console: String
  - quantidade: int
  - dataLancamento: LocalDate
  - preco: BigDecimal
  - foto: String
  - categoria: Categoria
  + getAll()
  + getById(Long id)
  + getByNome(String nome)
  + post(Produto produto)
  + put(Produto produto)
  + delete(Long id)
}
class Usuario {
  - id : Long
  - nome : String
  - usuario : String
  - senha : String
  - foto : String
  - dataNascimento : LocalDate
  - postagem : List ~Postagem~
  + getAll()
  + getById(Long id)
  + autenticarUsuario(UsuarioLogin usuarioLogin)
  + cadastrarUsuario(Usuario usuario)
  + atualizarUsuario(Usuario usuario)
  + delete(Long id)
}
class UsuarioLogin{
  - id : Long
  - nome : String
  - usuario : String
  - senha : String
  - foto : String
  - dataNascimento : LocalDate
  - token : String
}
Categoria --> Produto
```

<h2>Etapas:</h2>


- [x] Criar o Projeto Spring
- [x] Configurar as Dependências do Projeto
- [x] Configurar o Banco de dados
- [x] Criar a Camada Model
- [x] Criar a Camada Repository
- [x] Criar a Camada Controller
- [x] Criar o Relacionamento entre as 2 classes
- [x] Fazer os testes no Insomnia


<a href="https://lojagengames.herokuapp.com/" target="_blank">Deploy no Heroku</a>

