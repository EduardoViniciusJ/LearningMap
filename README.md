# LearningMap 

LearningMap é uma API backend desenvolvida em **.NET** que auxilia os usuários a estruturarem seu próprio **projeto de aprendizado**, com base nos princípios do mapa de **metaaprendizado**.  
Cada **mapa/projeto** contém informações organizadas sobre **Conhecimento**, **Estratégia** e **Motivação**, permitindo que o aprendizado seja planejado e mais eficiente.

---

## Tecnologias Utilizadas

- **.NET**
- **ASP.NET Core Web API**
- **Entity Framework Core**
- **ASP.NET Core Identity**
- **JWT Bearer Authentication**
- **AutoMapper**
- **Paginação**
- **SQL Server**
- **xUnit e FluentAssertions (Testes)**


## Funcionalidades

### Autenticação e Autorização
- Registro de usuários com validação de credenciais.
- Login com geração de **JWT**.
- Controle de acesso baseado em roles (`user`).

### Mapas/Projetos de Aprendizado
- Criar novos mapas/projetos, contendo **Conhecimento**, **Estratégia** e **Motivação**.
- Consultar todos os mapas ou um específico por ID.
- Atualizar ou remover mapas.
- Paginação de mapas com metadados no cabeçalho.

### Conhecimento
- Cadastro de itens que o usuário deseja aprender dentro de um mapa/projeto.
- Consultar conhecimentos por ID ou por mapa/projeto.
- Atualizar e remover conhecimentos.
- Paginação de resultados.

### Estratégia
- Cadastro de estratégias de aprendizado para cada mapa/projeto.
- Consultar estratégias por ID ou mapa/projeto.
- Atualizar e remover estratégias.
- Paginação de resultados.

### Motivação
- Cadastro de motivações que orientam o aprendizado.
- Consultar motivações por ID ou mapa/projeto.
- Atualizar e remover motivações.
- Paginação de resultados.

---

## Endpoints Principais

### Auth
- `POST /api/auth/register` → Registrar um novo usuário.
- `POST /api/auth/login` → Autenticar usuário e gerar token JWT.

### Mapas/Projetos
- `GET /api/projeto` → Listar todos os mapas/projetos.
- `GET /api/projeto/{id}` → Obter mapa/projeto por ID.
- `POST /api/projeto` → Criar um novo mapa/projeto básico.
- `POST /api/projeto/completo` → Criar um mapa/projeto completo com **Conhecimento**, **Estratégia** e **Motivação**.
- `PUT /api/projeto/{id}` → Atualizar mapa/projeto.
- `DELETE /api/projeto/{id}` → Deletar mapa/projeto.

### Conhecimento
- `GET /api/conhecimento` → Listar todos os conhecimentos.
- `GET /api/conhecimento/{id}/conhecimento` → Obter conhecimento por ID.
- `GET /api/conhecimento/{id}/projeto` → Obter conhecimentos de um mapa/projeto.
- `POST /api/conhecimento` → Criar conhecimento.
- `PUT /api/conhecimento/{projetoId}/conhecimento/{id}` → Atualizar conhecimento.
- `DELETE /api/conhecimento/{projetoId}/conhecimento/{id}` → Remover conhecimento.

### Estratégia
- `GET /api/estrategia` → Listar todas as estratégias.
- `GET /api/estrategia/{id}/estrategia` → Obter estratégia por ID.
- `GET /api/estrategia/{id}/projeto` → Obter estratégias de um mapa/projeto.
- `POST /api/estrategia` → Criar estratégia.
- `PUT /api/estrategia/{projetoId}/estrategia/{id}` → Atualizar estratégia.
- `DELETE /api/estrategia/{projetoId}/estrategia/{id}` → Remover estratégia.

### Motivação
- `GET /api/motivacao` → Listar todas as motivações.
- `GET /api/motivacao/{id}/motivacao` → Obter motivação por ID.
- `GET /api/motivacao/{id}/projeto` → Obter motivações de um mapa/projeto.
- `POST /api/motivacao` → Criar motivação.
- `PUT /api/motivacao/{projetoId}/motivacao/{id}` → Atualizar motivação.
- `DELETE /api/motivacao/{projetoId}/motivacao/{id}` → Remover motivação.

---

## Configuração do Projeto

1. Clone o repositório:
```bash
git clone <seu-repo>
cd MapL
