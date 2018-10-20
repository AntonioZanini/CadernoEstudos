# Transact-SQL (Microsoft)

## Artigos Importantes

- [https://social.technet.microsoft.com/wiki/pt-br/contents/articles/51485.sql-server-como-definir-o-tamanho-maximo-de-colunas-de-tamanho-variavel.aspx](https://social.technet.microsoft.com/wiki/pt-br/contents/articles/51485.sql-server-como-definir-o-tamanho-maximo-de-colunas-de-tamanho-variavel.aspx).
- [https://medium.com/@alexandre.malavasi/25-dicas-e-boas-pr%C3%A1ticas-de-banco-de-dados-para-desenvolvedores-7a60bfc28f1f](https://medium.com/@alexandre.malavasi/25-dicas-e-boas-pr%C3%A1ticas-de-banco-de-dados-para-desenvolvedores-7a60bfc28f1f).

## Conceitos

### Banco de Dados

Definição: Banco de dados é uma coleção de dados inter-relacionados, representando informações sobre um domínio específico. 

Ele é o objeto raiz de uma árvore que contém outros objetos distintos agindo de forma conjunta para abstrair e organizar dados sobre o domínio representado.

### Schema

Schema é um objeto que agrega outros objeto de modo a criar uma coleção. Esta coleção tem função organizacional e grande importância na segurança da informação.

## DDL (Data Definition Language ou Linguagem de Definição de Dados)

### CREATE

#### DATABASE

	CREATE DATABASE DBNAME;

Sobre o nome do banco de dados:
- Ele deve estar de acordo com as regras de **identificadores**;
- Seu tamanho dever ser um máximo de 128 caracteres;
- Convenções:
 - UPPERCASE. Ex: MEUBANCO.
 - Máximo de 30 caracteres.
 - [A-z].
 - Abreviável.		

[_Documentação_](https://docs.microsoft.com/pt-br/sql/t-sql/statements/create-database-transact-sql).

#### SCHEMA

	CREATE SCHEMA scmname [ AUTHORIZATION owner_name ];

Sobre o nome do schema:
- Ele deve estar de acordo com as regras de **identificadores**;
- Convenções:
 - lowercase. Ex: meuschema.
 - Máximo de 30 caracteres.
 - [A-z][0-9].
 - Abreviável.

[_Documentação_](https://docs.microsoft.com/pt-br/sql/t-sql/statements/create-schema-transact-sql).

#### TABLE

	CREATE TABLE MyTable (
		MyColumn01 int,
		MyColumn02 varchar[40]
	);





##### Reiniciar Chave de Identidade


DBCC CHECKIDENT ([NomeTabela], RESEED, NumeroBase);

NomeTabela - Nome da tabela com o campo de identidade, deve estar entre colchetes.

NumeroBase - Número anterior ao próximo valor desejado.

Ex.:

DBCC CHECKIDENT ([usuario.Usuario], RESEED, 2);
Reatribui o campo de identidade da tabela Usuário (dentro do schema usuario), o próximo registro terá o valor de 3.

## Regras Adicionais

### Regras para identificadores normais

Os nomes de variáveis, funções e procedimentos armazenados devem obedecer às regras de identificadores Transact-SQL .

1. O primeiro caractere deve ser um dos seguintes:

 - Uma letra, como definido pelo Unicode Standard 3.2. A definição de letras do Unicode inclui caracteres latinos de a até z, de A até Z, além de caracteres de letras de outros idiomas.

 - Sublinhado (), arroba (@) ou sinal de número (#).

 Determinados símbolos no começo de um identificador possuem um significado especial no SQL Server. Um identificador normal iniciado com arroba denota sempre uma variável local ou parâmetro e não pode ser utilizado como nome de qualquer outro tipo de objeto. Um identificador iniciado com um sinal de número denota uma tabela temporária ou procedimento. Um identificador iniciado com dois sinais de número (##) denota um objeto temporário global. Embora possa ser utilizado um caractere de sinal de número ou dois sinais de número para começar os nomes de outros tipos de objetos, não recomendamos essa prática.

 Algumas funções do Transact-SQL têm nomes iniciados com dois sinais de arroba (@@). Para evitar confusão com essas funções, você não deverá usar nomes iniciados por @@.

2. Os caracteres subsequentes podem incluir:

 - Letras, como definido no Unicode Standard 3.2.

 - Números decimais do latim básico ou outros scripts nacionais.

 - Arroba (@), cifrão ($), sinal de número (#) ou sublinhado.

3. O identificador não deve ser uma palavra reservada do Transact-SQL . SQL Server reserva as versões maiúscula e minúscula de palavras reservadas. Quando identificadores são usados nas instruções Transact-SQL , os identificadores que não estiverem de acordo com essas regras deverão ser delimitados por aspas duplas ou colchetes. As palavras reservadas dependem do nível de compatibilidade do banco de dados. Esse nível pode ser definido por meio da instrução ALTER DATABASE .

4. Não são permitidos espaços ou caracteres especiais.

5. Não são permitidos caracteres adicionais.

Quando identificadores são usados nas instruções Transact-SQL , os identificadores que não estiverem de acordo com essas regras deverão ser delimitados por aspas duplas ou colchetes.

[_Fonte e Documentação_](https://docs.microsoft.com/pt-br/sql/relational-databases/databases/database-identifiers).