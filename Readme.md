# Projeto Livraria

Bem-vindo ao projeto da API de uma **Livraria**. Esta aplicação é um backend completo para gerenciar clientes e compras, com funcionalidades de CRUD (Create, Read, Update, Delete) para ambas as entidades.

---

## 📖 Sobre o Projeto

O projeto foi construído utilizando o framework **Spring Boot** e segue uma arquitetura orientada a serviços. A API permite gerenciar clientes e registrar compras, com validações robustas e tratamento de erros para garantir a integridade dos dados.

### Funcionalidades Principais

* **Clientes:** Crie, visualize, altere, liste e exclua clientes.
* **Compras:** Registre novas compras, liste, visualize, altere e exclua.
* **Validação de Dados:** O sistema realiza validações em tempo real para garantir que os dados de entrada estejam corretos, evitando erros de negócio.
* **Tratamento de Erros:** Respostas de erro claras e informativas são fornecidas para facilitar a depuração.

---

## 🚀 Tecnologias Utilizadas

* **Java 17:** Linguagem de programação.
* **Spring Boot 2.x:** Framework para facilitar a criação de aplicações.
* **Spring Data JPA:** Para a persistência de dados.
* **ModelMapper:** Para o mapeamento de objetos DTO (Data Transfer Object) para entidades e vice-versa.
* **Lombok:** Para reduzir a verbosidade do código.
* **Maven:** Gerenciador de dependências e automação de builds.
* **Log4j2:** Para registro de logs da aplicação.
* **Validação Bean Validation (javax.validation):** Para validação de dados de entrada.

---

## ⚙️ Como Rodar a Aplicação

Para rodar o projeto localmente, siga os passos abaixo:

1.  **Pré-requisitos:** Certifique-se de ter o **JDK 17** e o **Maven** instalados na sua máquina.
2.  **Clone o repositório:**
    ```bash
    git clone [URL_DO_SEU_REPOSITORIO]
    cd [NOME_DO_SEU_PROJETO]
    ```
3.  **Configurar o Banco de Dados:** A aplicação utiliza um banco de dados relacional. Você precisará configurar as credenciais no arquivo `src/main/resources/application.properties`.
4.  **Compilar e Rodar:**
    ```bash
    mvn spring-boot:run
    ```
    A aplicação estará disponível em `http://localhost:8080`.

---

## 💻 Documentação da API

A seguir estão os endpoints disponíveis na API. Todas as requisições devem ser feitas para a URL base `http://localhost:8080/livraria`.

### Endpoints de Clientes

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| `POST` | `/livraria/cliente` | Cria um novo cliente. |
| `GET` | `/livraria/cliente/id/{id}` | Busca um cliente pelo ID. |
| `GET` | `/livraria/cliente` | Lista todos os clientes. |
| `PUT` | `/livraria/cliente/id/{id}` | Altera os dados de um cliente existente. |
| `DELETE`| `/livraria/cliente/id/{id}` | Exclui um cliente pelo ID. |

### Endpoints de Compras

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| `POST` | `/livraria/compra` | Cria uma nova compra. |
| `GET` | `/livraria/compra/id/{id}` | Busca uma compra pelo ID. |
| `GET` | `/livraria/compra` | Lista todas as compras. |
| `PUT` | `/livraria/compra/id/{id}` | Altera os dados de uma compra existente. |
| `DELETE`| `/livraria/compra/id/{id}` | Exclui uma compra pelo ID. |

### Tratamento de Erros

A API retorna códigos de status HTTP apropriados e objetos JSON com mensagens de erro claras, facilitando a identificação e a correção de problemas.

Exemplo de resposta de erro:

```json
{
  "codigoErro": 1001,
  "mensagem": "Cliente não encontrado.",
  "validacoes": []
}