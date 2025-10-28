[README .md](https://github.com/user-attachments/files/23176886/README.md)
# 🏆 Trabalho POO - Sistema Web com Spring Boot

Este projeto foi desenvolvido como parte da disciplina **Programação Orientada a Objetos (POO)**, com foco na criação de um **sistema web completo** utilizando o **framework Spring Boot**.

O sistema implementa todas as operações de um **CRUD (Create, Read, Update, Delete)** para gerenciar uma entidade **Time**, permitindo o **cadastro, listagem, edição, exclusão e visualização** de times de futebol, além do **upload de escudos**.

---

## ⚙️ Tecnologias Utilizadas

### 🖥️ Backend
- **Java 17**
- **Spring Boot**
  - **Spring Web** → Criação dos controladores e rotas da aplicação web.
  - **Spring Data JPA** → Persistência e manipulação de dados.
  - **Hibernate** → Implementação JPA.
- **H2 Database** → Banco de dados em modo arquivo, garantindo persistência após reinicialização.
- **Maven** → Gerenciamento de dependências e build (com Maven Wrapper `mvnw`).

### 🎨 Frontend
- **Thymeleaf** → Template engine para renderização das páginas HTML.
- **Bootstrap 5** → Estilização responsiva.
- **Bootstrap Icons (CDN)** → Ícones modernos e leves.

---

## 🧩 Funcionalidades Principais

| Funcionalidade | Descrição |
|----------------|------------|
| **Listar Times** (`/`) | Exibe todos os times cadastrados em uma tabela. |
| **Cadastrar Time** (`/cadastrar`) | Permite adicionar um novo time com upload obrigatório do escudo. |
| **Visualizar Time** (`/visualizar/{id}`) | Mostra os detalhes de um time específico. |
| **Editar Time** (`/editar/{id}`) | Edita as informações de um time, podendo atualizar o escudo. |
| **Excluir Time** (`/excluir/{id}`) | Remove o time e apaga o escudo correspondente da pasta `uploads/`. |

🗃️ **Persistência de Dados:**
- Banco de dados: `trabalho-db.mv.db`
- Escudos salvos na pasta: `uploads/`

---

## 🚀 Como Executar o Projeto

### ✅ Pré-requisitos
- Java **17** (ou superior)
- IDE com suporte a Maven (**IntelliJ IDEA**, **VSCode**, **Eclipse**, etc.)

---

### 🧠 Opção 1: Executar pela IDE (Recomendado)

1. Importe o projeto como **projeto Maven** na sua IDE.  
2. Aguarde o download das dependências do Maven.  
3. Localize o arquivo principal:  
   ```
   src/main/java/com/example/trabalho/TrabalhoAvaliativoApplication.java
   ```
4. Clique com o botão direito e selecione **Run 'TrabalhoAvaliativoApplication.main()'** ou pressione ▶️.

---

### 💻 Opção 2: Executar pelo Terminal

1. Abra o terminal na **pasta raiz do projeto** (onde está o arquivo `pom.xml`).  
2. Execute o comando correspondente ao seu sistema operacional:

#### Windows
```bash
.\mvnw.cmd spring-boot:run
```

#### Linux / macOS
```bash
./mvnw spring-boot:run
```

---

## 🌐 Acessando o Sistema

Após a inicialização do servidor, acesse:

- **Página Principal:** [http://localhost:8080](http://localhost:8080)  
- **Console do Banco de Dados (H2):** [http://localhost:8080/h2-console](http://localhost:8080/h2-console)

---

## 🗄️ Acesso ao Banco de Dados (H2 Console)

Para visualizar os dados diretamente no banco enquanto a aplicação está rodando:

1. Acesse [http://localhost:8080/h2-console](http://localhost:8080/h2-console)
2. Preencha os campos com as credenciais configuradas no `application.properties`:

| Campo | Valor |
|--------|--------|
| **Driver Class** | `org.h2.Driver` |
| **JDBC URL** | `jdbc:h2:file:./trabalho-db` |
| **User Name** | `sa` |
| **Password** | `password` |

3. Clique em **Conectar**.

---

## 📂 Estrutura do Projeto

```
trabalho-poo/
├── src/
│   ├── main/
│   │   ├── java/com/example/trabalho/
│   │   │   ├── controller/     # Controladores (rotas e lógicas)
│   │   │   ├── model/          # Entidades e classes de domínio
│   │   │   ├── repository/     # Interfaces JPA
│   │   │   ├── service/        # Regras de negócio (opcional)
│   │   │   └── TrabalhoAvaliativoApplication.java
│   │   └── resources/
│   │       ├── templates/      # Páginas HTML (Thymeleaf)
│   │       ├── static/         # CSS, JS, imagens, escudos
│   │       └── application.properties
├── uploads/                    # Pasta para armazenar escudos
├── trabalho-db.mv.db           # Arquivo do banco de dados H2
├── pom.xml                     # Configurações do Maven
└── README.md
```

---

## 💡 Observações

- O **upload de escudos** é obrigatório no cadastro e opcional na edição.  
- Ao **editar** um time e enviar um novo escudo, o arquivo antigo é automaticamente substituído.  
- Os dados são **persistentes** (não se perdem após encerrar a aplicação).  

---

## 👨‍💻 Autor

**Gustavo do Rosário Nunes**  
📚 Projeto acadêmico — Programação Orientada a Objetos  
🖥️ Desenvolvido com **Java 17**, **Spring Boot** e **Thymeleaf**

---

## 🏁 Licença

Este projeto é de uso educacional e pode ser livremente modificado ou reutilizado para fins de aprendizado.
