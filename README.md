# **Escola**

Aplicação para listar alunos do banco de dados "escola". Este projeto utiliza o framework Spring Boot e está configurado para se conectar a um banco de dados PostgreSQL.

## **Descrição**

O projeto "escola" é uma aplicação backend desenvolvida em Java com Spring Boot. Ele permite gerenciar e listar alunos armazenados em um banco de dados relacional. A aplicação utiliza JPA para interagir com o banco de dados e está configurada para rodar com Java 17.

## **Pré-requisitos**

Antes de executar o projeto, certifique-se de que você possui os seguintes itens instalados:

1. **
Java 17
** ou superior.
2. **
Maven
** para gerenciar as dependências e construir o projeto.
3. **
PostgreSQL
** como banco de dados relacional.
4. Uma IDE de sua preferência (IntelliJ IDEA, Eclipse, VS Code, etc.).

## **Configuração do Banco de Dados**

1. Crie um banco de dados no PostgreSQL com o nome `escola`.
2. Configure as credenciais de acesso ao banco de dados no arquivo `application.properties` ou `application.yml` da aplicação. Exemplo:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/escola
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```
## **Tecnologias Utilizadas**
- Java 17: Linguagem de programação.
- Spring Boot 3.4.2: Framework para desenvolvimento rápido de aplicações Java.
- Spring Data JPA: Para interação com o banco de dados.
- PostgreSQL: Banco de dados relacional.
- Lombok: Para reduzir o boilerplate de código.
- Maven: Gerenciador de dependências.
## **Dependências**
As principais dependências utilizadas no projeto estão listadas no arquivo pom.xml. Aqui estão algumas delas:

- spring-boot-starter-data-jpa
- spring-boot-starter-web
- postgresql
- lombok
## **Como Executar o Projeto**
1. Clone o repositório para sua máquina local:
```
git clone https://github.com/seu-usuario/escola.git
cd escola
```
2. Compile o projeto utilizando o Maven:
```
mvn clean install
```
## Execute a aplicação:
```
mvn spring-boot:run
```
*A aplicação estará disponível em: http://localhost:8080*

## Endpoints Disponíveis
**A aplicação expõe os seguintes endpoints:**
### GET /alunos
- Retorna a lista de todos os alunos cadastrados no banco de dados.
#### Exemplo de Resposta:
```
[
  {
    "id": 1,
    "nome": "João Silva",
    "idade": 20,
    "curso": "Engenharia"
  },
  {
    "id": 2,
    "nome": "Maria Oliveira",
    "idade": 22,
    "curso": "Medicina"
  }
]
```
## Estrutura do Projeto
**A estrutura do projeto segue o padrão do *Spring Boot*:**
```
src/
├── main/
│ ├── java/
│ │ └── com.zup.escola/
│ │ ├── controller/ # Controladores REST
│ │ ├── model/ # Modelos de dados
│ │ ├── repository/ # Repositórios JPA
│ │ └── service/ # Lógica de negócios
│ └── resources/
│ ├── application.properties # Configurações da aplicação
│ └── static/ # Arquivos estáticos (se necessário)
└── test/
└── java/ # Testes unitários e de integração
