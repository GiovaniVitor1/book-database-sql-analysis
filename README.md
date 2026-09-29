# 📚 Análise de Base de Livros com SQL

Projeto de análise de dados utilizando **SQL e PostgreSQL** para explorar uma base relacional composta por livros, autores, editoras, avaliações e resenhas de usuários.

O objetivo foi extrair informações relevantes do catálogo e identificar padrões que possam apoiar decisões relacionadas a conteúdo, engajamento e experiência do usuário.

## 🎯 Objetivos

As principais perguntas analisadas foram:

- quantos livros foram publicados após 1º de janeiro de 2000;
- qual o número de resenhas e a classificação média de cada livro;
- qual editora possui mais livros com mais de 50 páginas;
- qual autor possui a maior classificação média entre livros com volume mínimo de avaliações;
- qual o nível de engajamento dos usuários mais ativos.

## 🗃️ Estrutura dos dados

A análise utiliza cinco tabelas principais:

| Tabela | Conteúdo |
|---|---|
| `books` | informações dos livros |
| `authors` | autores |
| `publishers` | editoras |
| `ratings` | classificações numéricas |
| `reviews` | resenhas textuais |

As relações entre as tabelas são realizadas principalmente por meio de:

- `book_id`
- `author_id`
- `publisher_id`
- `username`

## 🔎 Principais análises

### Livros publicados após 2000

Foram identificados:

**819 livros publicados após 1º de janeiro de 2000.**

Esse resultado ajuda a compreender a composição temporal do catálogo.

### Número de resenhas e classificação média

Foi criada uma consulta para calcular, para cada livro:

- quantidade de resenhas;
- média das classificações recebidas.

As métricas de `ratings` e `reviews` foram tratadas separadamente para evitar duplicação de registros durante os `JOINs`.

### Editora com mais livros

Considerando apenas livros com mais de **50 páginas**, a editora com maior quantidade de títulos foi:

**Penguin Books — 42 livros**

Esse resultado indica forte presença da editora no catálogo analisado.

### Autor com maior média de classificação

Considerando apenas livros com pelo menos **50 classificações**, o maior resultado foi:

**J.K. Rowling/Mary GrandPré — média aproximada de 4,29**

O filtro mínimo de avaliações foi utilizado para evitar que livros com poucas classificações influenciassem excessivamente o resultado.

### Engajamento dos usuários

A análise também avaliou usuários que classificaram mais de **50 livros**.

Foi feita uma separação entre:

- classificações numéricas;
- resenhas textuais.

Essa distinção permite avaliar diferentes níveis de engajamento dos usuários com a plataforma.

## 📌 Principais conclusões

A análise demonstrou como consultas SQL podem ser utilizadas para transformar uma base relacional em informações relevantes para o negócio.

Entre os principais resultados:

- **819 livros** foram publicados após 2000;
- **Penguin Books** apresentou a maior quantidade de livros com mais de 50 páginas;
- **J.K. Rowling/Mary GrandPré** apresentou uma das maiores médias entre autores com livros suficientemente avaliados;
- usuários altamente ativos representam um segmento relevante para funcionalidades de recomendação e comunidade.

## 💡 Possíveis aplicações

Os resultados poderiam apoiar funcionalidades como:

- recomendações personalizadas;
- rankings de livros;
- destaque de autores e editoras;
- filtros por popularidade e avaliação;
- identificação de usuários altamente engajados;
- incentivo à criação de resenhas.

## 🛠️ Tecnologias utilizadas

- SQL
- PostgreSQL
- Python
- Pandas
- SQLAlchemy
- Jupyter Notebook
- Git
- GitHub

## 📁 Estrutura do repositório

```text
book-database-sql-analysis/
│
├── book_database_sql_portfolio.ipynb
│
└── README.md
```

## 📓 Notebook

O notebook contém:

- conexão com banco PostgreSQL;
- inspeção inicial das tabelas;
- consultas SQL;
- `JOINs`;
- agregações;
- `GROUP BY`;
- subconsultas;
- CTEs;
- interpretação dos resultados;
- conclusão geral.

➡️ [`book_database_sql_portfolio.ipynb`](book_database_sql_portfolio.ipynb)

---

### Autor

**Giovani Vitor Gabriel Oliveira**

[LinkedIn](https://www.linkedin.com/in/giovani-vitor-4b04172a3/) | [GitHub](https://github.com/GiovaniVitor1)
