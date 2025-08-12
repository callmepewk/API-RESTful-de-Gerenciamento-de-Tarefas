API RESTful de Gerenciamento de Tarefas

Projeto desenvolvido como parte do *Trabalho de Desenvolvimento Web Back-end*

Professora: Luciane Kanashiro, Me  

Aluno: Pedro Henrique Brezolin de Freitas 

RU: 4683201


Objetivo
Implementar uma **API RESTful** para gerenciamento de tarefas utilizando **Java com Spring Boot**, permitindo:
- Criar tarefas
- Listar tarefas
- Buscar tarefa por ID
- Atualizar tarefa
- Remover tarefa

Cada tarefa possui:
- **id** (gerado automaticamente)
- **nome** (String)
- **dataEntrega** (Data)
- **responsavel** (String)


Tecnologias Utilizadas
- **Java 17**
- **Spring Boot 3**
- **Spring Web**
- **Spring Data JPA**
- **MySQL**
- **Hibernate**
- **Postman** (testes e documentação)


Estrutura do Projeto:

src/main/java/com/exemplo/tarefas/

├── TarefasApplication.java # Classe principal

├── model/

│ └── Tarefa.java # Entidade

├── repository/

│ └── TarefaRepository.java # Repositório JPA

├── service/

│ └── TarefaService.java # Lógica de negócio

├── controller/

│ └── TarefaController.java # Endpoints REST

└── exception/

├── ResourceNotFoundException.java

└── GlobalExceptionHandler.java


Configuração do Banco de Dados

No arquivo `src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/tarefas_db?useSSL=false&serverTimezone=UTC
spring.datasource.username=SEU_USUARIO
spring.datasource.password=SUA_SENHA

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
