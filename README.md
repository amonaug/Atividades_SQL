# Curso de Banco de Dados - Atividades no VRBox

Este repositório contém os scripts e consultas desenvolvidos durante o curso de Banco de Dados, com atividades realizadas no ambiente **VRBox**. Os scripts incluem a criação de banco de dados, tabelas e execução de consultas SQL para diferentes cenários de aprendizado.

## Descrição Geral
O objetivo das atividades é explorar os conceitos básicos e avançados de SQL, como:
- Criação de banco de dados e tabelas.
- Inserção de registros.
- Execução de consultas simples e com filtros.
- Manipulação e organização de dados.

## Scripts Disponíveis

### Criação do Banco de Dados e Tabela
```sql
CREATE DATABASE LIVRARIA;

USE LIVRARIA;

CREATE TABLE LIVRO(
    NOME_LIVRO VARCHAR(60),
    NOME_AUTOR VARCHAR(60),
    SEXO_AUTOR CHAR(1),
    NUMERO_PAGINAS INT(6),
    NOME_EDITORA VARCHAR(60),
    VALOR_LIVRO FLOAT(6, 2),
    UF_EDITORA CHAR(2),
    ANO_PUBLICACAO INT(4)
);
```

### Inserção de Dados
```sql
INSERT INTO LIVRO(NOME_LIVRO, NOME_AUTOR, SEXO_AUTOR, NUMERO_PAGINAS, NOME_EDITORA, VALOR_LIVRO, 
UF_EDITORA, ANO_PUBLICACAO) 
VALUES('CAVALEIRO REAL', 'ANA CLAUDIA', 'F', 465, 'ATLAS', 49.9, 'RJ', 2009);

INSERT INTO LIVRO(NOME_LIVRO, NOME_AUTOR, SEXO_AUTOR, NUMERO_PAGINAS, NOME_EDITORA, VALOR_LIVRO, 
UF_EDITORA, ANO_PUBLICACAO) 
VALUES('SQL Para Leigos', 'João Nunes', 'M', 450, 'Addison', 98, 'SP', 2018);
```

### Consultas SQL

```sql
-- Trazer todos os dados da tabela:
SELECT * FROM LIVRO;

-- Trazer o nome do livro e da editora:
SELECT NOME_LIVRO AS LIVRO, NOME_EDITORA AS EDITORA FROM LIVRO;

-- Filtrar livros publicados por autores do sexo masculino:
SELECT NOME_LIVRO AS LIVRO, UF_EDITORA AS ESTADO_DA_EDITORA FROM LIVRO
WHERE SEXO_AUTOR = 'M';

-- Filtrar livros publicados por autores do sexo feminino:
SELECT NOME_LIVRO AS LIVRO, NUMERO_PAGINAS AS PAGINAS FROM LIVRO
WHERE SEXO_AUTOR = 'F';

-- Trazer livros publicados por editoras de São Paulo:
SELECT VALOR_LIVRO AS VALOR FROM LIVRO
WHERE UF_EDITORA = 'SP';
```

## Como Utilizar
1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```
2. Abra os scripts no seu editor SQL ou no ambiente VRBox.
3. Execute os comandos sequencialmente para criar, popular e consultar o banco de dados.

## Contribuições
Contribuições são bem-vindas! Envie um pull request com melhorias ou novas ideias.

## Licença
Este repositório está licenciado sob a Licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.

