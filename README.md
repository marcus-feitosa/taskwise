# taskwise

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: <https://quarkus.io/>.

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:

```shell script
./mvnw quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at <http://localhost:8080/q/dev/>.

## Packaging and running the application

The application can be packaged using:

```shell script
./mvnw package
```

It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:

```shell script
./mvnw package -Dquarkus.package.jar.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable

You can create a native executable using:

```shell script
./mvnw package -Dnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

```shell script
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/taskwise-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult <https://quarkus.io/guides/maven-tooling>.

## Related Guides

- REST ([guide](https://quarkus.io/guides/rest)): A Jakarta REST implementation utilizing build time processing and Vert.x. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it.
- Hibernate ORM ([guide](https://quarkus.io/guides/hibernate-orm)): Define your persistent model with Hibernate ORM and Jakarta Persistence
- JDBC Driver - PostgreSQL ([guide](https://quarkus.io/guides/datasource)): Connect to the PostgreSQL database via JDBC

## Provided Code

### Hibernate ORM

Create your first JPA entity

[Related guide section...](https://quarkus.io/guides/hibernate-orm)



### REST

Easily start your REST Web Services

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)



##DEFINICAO DE REQUISITOS GERADA POR IA
ome do Projeto: "TaskWise" (sinta-se à vontade para sugerir um nome melhor depois!)

Visão Geral: O TaskWise é um aplicativo web simples e intuitivo que permite aos usuários gerenciar suas tarefas diárias. O objetivo principal é fornecer uma plataforma eficiente para criar, organizar, acompanhar e concluir tarefas.

Público-Alvo: Indivíduos que desejam uma ferramenta simples e eficaz para organizar suas atividades pessoais ou profissionais.

Requisitos Funcionais (O que o sistema deve fazer):

Cadastro e Login de Usuários:

RF01: O sistema deve permitir que novos usuários se cadastrem fornecendo um nome de usuário, endereço de e-mail e senha.
RF02: O sistema deve permitir que usuários existentes façam login utilizando seu nome de usuário/e-mail e senha.
RF03: O sistema deve implementar um mecanismo de recuperação de senha (por exemplo, envio de e-mail com link para redefinição).
RF04: As senhas devem ser armazenadas de forma segura (hash e salt).
Gerenciamento de Tarefas:

RF05: O sistema deve permitir que usuários criem novas tarefas, definindo um título, uma descrição (opcional) e uma data de vencimento (opcional).
RF06: O sistema deve permitir que usuários visualizem todas as suas tarefas.
RF07: O sistema deve permitir que usuários marquem tarefas como concluídas.
RF08: O sistema deve permitir que usuários editem o título, a descrição e a data de vencimento de uma tarefa existente.
RF09: O sistema deve permitir que usuários excluam tarefas.
Organização de Tarefas:

RF10: O sistema deve permitir que usuários categorizem suas tarefas (por exemplo, "Pessoal", "Trabalho", "Estudos").
RF11: O sistema deve permitir que usuários definam a prioridade de uma tarefa (por exemplo, "Alta", "Média", "Baixa").
RF12: O sistema deve permitir que usuários filtrem suas tarefas por status (pendentes, concluídas), categoria e prioridade.
RF13: O sistema deve permitir que usuários ordenem suas tarefas por data de criação, data de vencimento ou prioridade.
Notificações (MVP Opcional, mas interessante para o futuro):

RF14 (Futuro): O sistema poderia enviar notificações por e-mail ou no aplicativo lembrando os usuários de tarefas com vencimento próximo.
Regras de Negócio (As políticas e restrições do sistema):

RB01: Cada tarefa deve pertencer a um único usuário.
RB02: O título da tarefa é obrigatório e deve ter um limite máximo de caracteres (a definir, por exemplo, 100 caracteres).
RB03: A data de vencimento, se definida, deve ser uma data futura ou o dia atual.
RB04: Um usuário deve estar logado para criar, visualizar, editar, marcar como concluída ou excluir tarefas.
RB05: As categorias e prioridades podem ser predefinidas pelo sistema (por exemplo, ao criar uma tarefa, o usuário escolhe entre as opções existentes) ou, em uma versão futura, permitir a criação de novas categorias pelo usuário.
RB06: Ao marcar uma tarefa como concluída, ela deve ser movida para uma seção de "Tarefas Concluídas" (a forma de visualização fica a seu critério).
RB07: A exclusão de uma tarefa deve ser uma ação irreversível (talvez com uma confirmação para evitar exclusões acidentais).
RB08: O nome de usuário e o e-mail devem ser únicos no sistema durante o cadastro.
Requisitos Não Funcionais (Qualidades do sistema):

RNF01: Desempenho: O sistema deve ser responsivo e carregar as informações rapidamente.
RNF02: Segurança: As informações dos usuários e das tarefas devem ser armazenadas de forma segura.
RNF03: Usabilidade: A interface deve ser intuitiva e fácil de usar.
RNF04: Escalabilidade (Consideração Futura): O sistema deve ser projetado de forma a poder suportar um número crescente de usuários e tarefas no futuro.
RNF05: Manutenibilidade: O código deve ser bem estruturado e fácil de manter.
