# Sistema de Gerenciamento de Biblioteca

Este é um sistema básico de gerenciamento de biblioteca utilizando SQLite. O sistema inclui as seguintes funcionalidades:
- Gerenciamento de autores
- Gerenciamento de livros
- Controle de empréstimos de livros

## Estrutura do Banco de Dados

### Tabelas

1. **Autores**
   - `AutorID`: ID único do autor (chave primária)
   - `Nome`: Nome do autor
   - `Nacionalidade`: Nacionalidade do autor

2. **Livros**
   - `LivroID`: ID único do livro (chave primária)
   - `Titulo`: Título do livro
   - `AutorID`: ID do autor que escreveu o livro (chave estrangeira)
   - `AnoPublicacao`: Ano de publicação do livro
   - `Genero`: Gênero do livro

3. **Empréstimos**
   - `EmprestimoID`: ID único do empréstimo (chave primária)
   - `LivroID`: ID do livro emprestado (chave estrangeira)
   - `DataEmprestimo`: Data em que o livro foi emprestado
   - `DataDevolucao`: Data em que o livro foi devolvido (pode ser `NULL` se ainda não devolvido)
   - `NomeUsuario`: Nome do usuário que fez o empréstimo
