Sistema-de-Gerenciamento-de-Times
Java-Spring WEB

Este projeto é focado no desenvolvimento de um sistema web completo utilizando Spring Boot.

O sistema implementa todas as operações de um CRUD (Create, Read, Update, Delete) para gerenciar uma entidade Time. A funcionalidade principal inclui o cadastro de times de futebol, permitindo o upload de uma atualização de escudos de cada time.

Tecnologias Utilizadas
Backend: Java 17 e Spring Boot
Spring Web: Para a criação dos controladores e da aplicação web.
Spring Data JPA: Para persistência de dados e comunicação com o banco.
Hibernate: Como implementar o JPA (ativado com spring.jpa.hibernate.ddl-auto=update).
Frontend: Thymeleaf (para renderização das páginas HTML no lado do servidor).
Banco de Dados: H2 Database (configurado em modo arquivo , para que os dados persistam após o reinício da aplicação).
Build: Apache Maven (utilizando o Maven Wrapper mvnw).
Estilização: Bootstrap 5 e Bootstrap Icons (via CDN) para um layout responsivo e moderno.
Funcionalidades Principais
Listar Tempos ( /): Página principal que exibe todos os tempos cadastrados em uma tabela.
Cadastrar Time ( /cadastrar): Formulário para adicionar um novo time, incluindo o upload obrigatório do arquivo de escudo.
Visualizar Horário ( /visualizar/{id}): Página de detalhes que exibe as informações de um horário específico.
Editar Tempo ( /editar/{id}): Formulário para alterar os dados de um tempo. Permite enviar um novo escudo (que substitui e apaga o antigo) ou manter o escudo atual.
Excluir Time ( /excluir/{id}): Remove um time do banco de dados e também exclui seu arquivo de escudo da pasta uploads/.
Persistência de Dados: O banco de dados ( trabalho-db.mv.db) e os escudos ( uploads/) são salvos na raiz do projeto.
Como Executar o Projeto
É necessário ter o Java 17 (ou superior) instalado na máquina.

Opção 1: Pela IDE (Recomendado)
Importe o projeto como um projeto Maven em seu IDE (IntelliJ, VSCode ou Eclipse).
Espere um IDE baixar todas as dependências do Maven.
Encontre o arquivo src/main/java/com/example/trabalho/TrabalhoAvaliativoApplication.java.
Clique com o botão direito e execute o método main()(ou clique no ícone de "play" ▶).
Opção 2: Terminal Pelo
Abra um terminal (Prompt de Comando ou PowerShell) na pasta raiz do projeto (onde está o arquivo pom.xml).

Execute o seguinte comando:

# No Windows
.\mvnw.cmd spring-boot:run

# No Linux ou macOS
./mvnw spring-boot:run
Acessando o Sistema
Após a inicialização do servidor, acesse os seguintes endereços no seu navegador:

Página Principal: http://localhost:8080
Console do Banco de Dados: http://localhost:8080/h2-console
Acesso ao Banco de Dados (Console H2)
Para visualizar os dados diretamente no banco enquanto a aplicação está rodando:

Acessohttp://localhost:8080/h2-console
Na tela de login, insira as credenciais abaixo (as mesmas do application.properties):
Classe de motorista: org.h2.Driver
URL do JDBC: jdbc:h2:file:./trabalho-db
Nome de usuário: sa
Senha: password
Clique em "Conectar" .