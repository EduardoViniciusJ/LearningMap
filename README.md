# LearningMap

LearningMap é uma API backend desenvolvida em **.NET** que auxilia os usuários a estruturarem seu próprio processo de aprendizado, com base nos princípios do **metaaprendizado**. A aplicação permite criar "mapas" de aprendizado com informações organizadas em **Conhecimento**, **Estratégia** e **Motivação**, garantindo um aprendizado mais eficiente e planejado.

---

## Tecnologias Utilizadas

- **.NET 8**
- **ASP.NET Core Web API**
- **Entity Framework Core 9**
- **ASP.NET Core Identity**
- **JWT Bearer Authentication**
- **AutoMapper**
- **Swagger**
- **SQL Server**
- **xUnit e FluentAssertions Testes**

---

## Funcionalidades

### Autenticação e Autorização
- Registro de usuários com validação de credenciais.
- Login com geração de **JWT**.
- Controle de acesso baseado em roles (`user`).

### Gerenciamento de Projetos de Aprendizado
- CRUD completo para **Projetos**.
- Suporte para criação de projetos completos com todos os detalhes (Conhecimento, Estratégia e Motivação).
- Paginação de projetos com metadados no cabeçalho (`X-Pagination`).

### Conhecimento
- Cadastro de itens de conhecimento que o usuário deseja aprender.
- Consultar conhecimentos por ID ou projeto.
- Atualizar e remover conhecimentos.
- Paginação de resultados.

### Estratégia
- Cadastro de estratégias de aprendizado.
- Consultar estratégias por ID ou projeto.
- Atualizar e remover estratégias.
- Paginação de resultados.

### Motivação
- Cadastro de motivações para os projetos.
- Consultar motivações por ID ou projeto.
- Atualizar e remover motivações.
- Paginação de resultados.

---
## Endpoints 

### Auth
- `POST /api/auth/register` → Registrar um novo usuário.
- `POST /api/auth/login` → Autenticar usuário e gerar token JWT.

### Projetos
- `GET /api/projeto` → Listar todos os projetos.
- `GET /api/projeto/{id}` → Obter projeto por ID.
- `POST /api/projeto` → Criar projeto.
- `POST /api/projeto/completo` → Criar projeto completo.
- `PUT /api/projeto/{id}` → Atualizar projeto.
- `DELETE /api/projeto/{id}` → Deletar projeto.

### Conhecimento
- `GET /api/conhecimento` → Listar todos os conhecimentos.
- `GET /api/conhecimento/{id}/conhecimento` → Obter conhecimento por ID.
- `GET /api/conhecimento/{id}/projeto` → Obter conhecimentos de um projeto.
- `POST /api/conhecimento` → Criar conhecimento.
- `PUT /api/conhecimento/{projetoId}/conhecimento/{id}` → Atualizar conhecimento.
- `DELETE /api/conhecimento/{projetoId}/conhecimento/{id}` → Remover conhecimento.

### Estratégia
- `GET /api/estrategia` → Listar todas as estratégias.
- `GET /api/estrategia/{id}/estrategia` → Obter estratégia por ID.
- `GET /api/estrategia/{id}/projeto` → Obter estratégias de um projeto.
- `POST /api/estrategia` → Criar estratégia.
- `PUT /api/estrategia/{projetoId}/estrategia/{id}` → Atualizar estratégia.
- `DELETE /api/estrategia/{projetoId}/estrategia/{id}` → Remover estratégia.

### Motivação
- `GET /api/motivacao` → Listar todas as motivações.
- `GET /api/motivacao/{id}/motivacao` → Obter motivação por ID.
- `GET /api/motivacao/{id}/projeto` → Obter motivações de um projeto.
- `POST /api/motivacao` → Criar motivação.
- `PUT /api/motivacao/{projetoId}/motivacao/{id}` → Atualizar motivação.
- `DELETE /api/motivacao/{projetoId}/motivacao/{id}` → Remover motivação.
