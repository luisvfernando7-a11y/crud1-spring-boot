# Product CRUD API — Spring Boot

API REST para gerenciamento de produtos, desenvolvida com Java e Spring Boot.

![Java](https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.5-brightgreen?style=flat-square&logo=springboot)
![H2](https://img.shields.io/badge/H2-Database-blue?style=flat-square)
![Gradle](https://img.shields.io/badge/Gradle-8.x-02303A?style=flat-square&logo=gradle)
![Status](https://img.shields.io/badge/status-concluído-success?style=flat-square)

---

## Sobre

API REST com as 4 operações do CRUD (Create, Read, Update, Delete) para gerenciamento de produtos. Desenvolvida com Spring Boot, Spring Data JPA e banco de dados H2 em memória.

---

## Tecnologias

| Tecnologia | Versão | Uso |
|---|---|---|
| Java | 17 | Linguagem principal |
| Spring Boot | 3.2.5 | Framework web |
| Spring Data JPA | — | Persistência de dados |
| H2 Database | — | Banco em memória |
| Lombok | — | Redução de boilerplate |
| Gradle | 8.x | Gerenciador de build |

---

## Estrutura do projeto

```
src/
└── main/
    ├── java/com/crud1/
    │   ├── Crud1Application.java      # Ponto de entrada
    │   ├── Product.java               # Entidade / tabela no banco
    │   ├── ProductRepository.java     # Acesso ao banco de dados
    │   └── ProductController.java     # Endpoints REST
    └── resources/
        └── application.properties     # Configurações
```

---

## Endpoints

| Método | URL | Descrição |
|--------|-----|-----------|
| `POST` | `/products` | Criar produto |
| `GET` | `/products` | Listar todos os produtos |
| `GET` | `/products/{id}` | Buscar produto por ID |
| `PUT` | `/products/{id}` | Atualizar produto |
| `DELETE` | `/products/{id}` | Deletar produto |

---

## Exemplos de requisição

**Criar produto**
```http
POST http://localhost:8080/products
Content-Type: application/json

{
  "name": "Camiseta",
  "priceInCents": 4990
}
```

**Resposta**
```json
{
  "id": 1,
  "name": "Camiseta",
  "priceInCents": 4990
}
```

**Listar todos**
```http
GET http://localhost:8080/products
```

**Buscar por ID**
```http
GET http://localhost:8080/products/1
```

**Atualizar**
```http
PUT http://localhost:8080/products/1
Content-Type: application/json

{
  "name": "Camiseta Atualizada",
  "priceInCents": 5990
}
```

**Deletar**
```http
DELETE http://localhost:8080/products/1
```

---

## Como rodar localmente

**Pré-requisitos**
- Java 17 ou superior
- IntelliJ IDEA ou outra IDE Java

**Instalação**

```bash
git clone https://github.com/luisvfernando7-a11y/crud1-spring-boot.git
cd crud1-spring-boot
```

Abra o projeto na IDE e execute a classe `Crud1Application`.

A API estará disponível em `http://localhost:8080`.

**Console do banco H2**

O banco de dados pode ser acessado visualmente pelo navegador durante a execução:

```
URL:      http://localhost:8080/h2-console
JDBC URL: jdbc:h2:mem:testdb
User:     sa
Password: (deixe vazio)
```

---

## Aprendizados

- Estrutura e configuração de projeto Spring Boot com Gradle
- Mapeamento de entidades JPA e criação automática de tabelas
- Uso do Spring Data JPA com `JpaRepository`
- Construção de endpoints REST com `@RestController`
- Validação de dados com Bean Validation (`@NotBlank`, `@Positive`)
- Injeção de dependências com `@Autowired`
- Testes de API com HTTP Client do IntelliJ IDEA

---

## Autor

**Luis Fernando**

[![Portfolio](https://img.shields.io/badge/Portfolio-luisgalvani.vercel.app-black?style=flat-square&logo=vercel)](https://luisgalvani.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-luisfernandovieira-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/luisfernandovieira)
[![GitHub](https://img.shields.io/badge/GitHub-luisvfernando7--a11y-181717?style=flat-square&logo=github)](https://github.com/luisvfernando7-a11y)
[![Email](https://img.shields.io/badge/Email-luisvfernando7@gmail.com-D14836?style=flat-square&logo=gmail)](mailto:luisvfernando7@gmail.com)
