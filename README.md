# Infraestrutura Docker para CRUD

Criação de uma infraestrutura completa e portável utilizando Docker para executar uma aplicação CRUD em PHP, garantindo que o ambiente seja facilmente replicável com um único comando.

---

## 🛠️ Tecnologias Utilizadas

* **Docker & Docker Compose:** Para orquestração dos contêineres.
* **PHP 8.2 (com Apache):** Como ambiente para a execução da aplicação CRUD.
* **MySQL 8.0:** Como banco de dados para persistência dos dados.
* **Adminer:** Como ferramenta para gerenciamento visual do banco de dados.

---

## 📂 Estrutura do Projeto

O repositório está organizado da seguinte forma:

```
/
├── app/
│   ├── Dockerfile
│   └── index.php
│
├── docker-compose.yml
└── script_sql.sql
```

---

## 🚀 Como Executar

A execução do projeto é simples e direta, conforme solicitado.

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/gabrieltangerina/AtividadeDocker-P2.git
    ```

2.  **Acesse o diretório do projeto:**
    ```bash
    cd AtividadeDocker-P2/
    ```

3.  **Inicie os contêineres:**
    ```bash
    docker compose up -d
    ```
    O comando irá construir a imagem customizada do PHP, baixar as imagens necessárias e iniciar todos os serviços em segundo plano (`-d`).

    > ⚠️ **Atenção:**
    >
    > Após iniciar os contêineres, aguarde alguns segundos. O banco de dados pode demorar um pouco mais para inicializar. Se você encontrar um erro de conexão com o banco na primeira vez que carregar a página, basta atualizá-la (F5).

---

## 🔗 Acessando os Serviços

Após a inicialização dos contêineres, os serviços expõem as seguintes portas em sua máquina (`localhost`). Você pode usar os endereços abaixo para interagir com cada parte da aplicação:

| Serviço              | Porta Exposta | 
| :------------------- | :------------ | 
| **Aplicação CRUD** | `80`          |
| **Adminer** | `8080`        |
| **Banco de Dados** | `3306`        |

### Login no Adminer
Para acessar o banco de dados através do Adminer, utilize as seguintes credenciais na tela de login:

* **Sistema:** `MySQL`
* **Servidor:** `mysql`
* **Usuário:** `gabriel`
* **Senha:** `senha_da_nasa`
* **Banco de Dados:** `crud_db`
