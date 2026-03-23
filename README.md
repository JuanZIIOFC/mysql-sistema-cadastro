# Sistema de Cadastro - Banco de Dados MySQL

Projeto prático focado na modelagem e criação de um banco de dados relacional (MySQL). O cenário do projeto é um sistema de cadastro escolar, onde temos alunos (gafanhotos) e cursos, e precisamos registrar de forma eficiente quais alunos estão matriculados em quais cursos.

## Detalhes Técnicos do Projeto
* **Estruturação (DDL):** Criação das tabelas `gafanhotos` e `cursos` com definição de tipos de dados (VARCHAR, INT, DATE, ENUM, DECIMAL), constraints e chaves primárias (AUTO_INCREMENT).
* **Relacionamento 1:N:** Adição da chave estrangeira `cursopreferido` na tabela de alunos usando `ALTER TABLE`, referenciando a tabela de cursos.
* **Relacionamento N:M (Muitos para Muitos):** Para resolver a regra de negócio onde um aluno pode fazer vários cursos e um curso tem vários alunos, criei a entidade associativa (tabela de junção) `gafanhotos_assiste_curso`, garantindo a integridade dos dados sem duplicidade.
* **Manipulação e Consultas (DML):** Inserção massiva de dados para testes (`INSERT INTO`) e criação de consultas cruzando as três tabelas utilizando `JOIN`, além de filtros com `WHERE`, `GROUP BY` e `HAVING`.

## Como rodar o banco
1. Clone este repositório.
2. Importe o script `Dump2026-03-23.sql` no seu SGBD (MySQL Workbench, phpMyAdmin, DBeaver, etc). O script já cria toda a estrutura e popula as tabelas automaticamente.

**Referências:**
Baseado nos exercícios e desafios do curso de Banco de Dados do professor Gustavo Guanabara (Curso em Vídeo).
Link da playlist: https://www.youtube.com/playlist?list=PLHz_AreHm4dkBs-795Dsgvau_ekxg8g1r
