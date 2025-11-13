
# ✔️ Projeto 1 — To-Do App (CRUD de Tarefas)

Este é o primeiro projeto da trilogia de aprendizado Fullstack.
Aqui você vai construir uma aplicação completa de gerenciamento de tarefas, com **frontend + backend + banco de dados**, aprendendo na prática os fundamentos essenciais de desenvolvimento web.

---

# 📌 Objetivo do Projeto

Criar uma aplicação web simples e funcional para gerenciar tarefas, permitindo:

* **Criar** novas tarefas
* **Listar** tarefas cadastradas
* **Editar** uma tarefa existente
* **Excluir** tarefa
* **Filtrar** por status (pendente/concluída)
* **Marcar tarefa como concluída**

Este projeto representa o **primeiro nível** do ciclo de aprendizado — focado em CRUD, APIs REST e integração front↔back.

---

# 🧱 Tecnologias Utilizadas

### **Backend**

* Node.js
* Express
* Prisma ORM
* SQLite ou PostgreSQL
* TypeScript (opcional)

### **Frontend**

* React ou Next.js
* Axios / Fetch API
* CSS/Tailwind/Bootstrap (livre escolha)

---

# 📂 Estrutura Geral do Projeto

```
/todo-fullstack
  /backend
    prisma/
    src/
      routes/
      controllers/
      services/
      server.ts
    package.json

  /frontend
    src/
      components/
      pages/ (ou views)
    package.json

  README.md
```

---

# 🗄️ Modelagem da Tarefa

**Modelo básico (Prisma):**

| Campo      | Tipo        | Descrição                 |
| ---------- | ----------- | ------------------------- |
| id         | string/uuid | Identificador único       |
| titulo     | string      | Nome da tarefa            |
| descricao  | string?     | Detalhes da tarefa        |
| dataLimite | Date?       | Prazo                     |
| status     | string      | 'pendente' ou 'concluida' |
| createdAt  | Date        | Data de criação           |

---

# 🔌 Endpoints da API

### **GET /tasks**

Lista todas as tarefas.

### **GET /tasks/:id**

Retorna detalhes de uma tarefa.

### **POST /tasks**

Cria uma nova tarefa.
Exemplo de body:

```json
{
  "titulo": "Estudar React",
  "descricao": "Focando em hooks e states",
  "dataLimite": "2025-02-10",
  "status": "pendente"
}
```

### **PUT /tasks/:id**

Atualiza uma tarefa existente.

### **DELETE /tasks/:id**

Exclui uma tarefa.

---

# 💻 Funcionalidades do Frontend

* Tela inicial exibindo lista de tarefas
* Formulário para criar tarefa
* Botão para editar uma tarefa
* Botão para excluir
* Botão “Concluir” (altera status via API)
* Filtro por status:

  * Todas
  * Pendentes
  * Concluídas

---

# ▶️ Como Rodar o Projeto

## 1️⃣ Clonar repositório

```
git clone https://github.com/seu-usuario/todo-fullstack
cd todo-fullstack
```

---

## 2️⃣ Rodar o Backend

```
cd backend
npm install
```

Configurar o `.env`:

```
DATABASE_URL="file:./dev.db"
```

Rodar migrações:

```
npx prisma migrate dev
```

Iniciar servidor:

```
npm run dev
```

Backend padrão:

```
http://localhost:3001
```

---

## 3️⃣ Rodar o Frontend

```
cd frontend
npm install
npm run dev
```

Frontend padrão:

```
http://localhost:3000
```

---

# 📸 Prints / Demonstração (opcional)

Adicione aqui imagens das telas quando terminar o projeto:

```
/docs
   tela-lista.png
   tela-criacao.png
   tela-edicao.png
```

---

# 🧠 O que você aprende com este projeto

* Como estruturar um backend com rotas, controllers e services
* Como criar um CRUD completo
* Como usar Prisma ORM
* Como integrar frontend e backend em uma aplicação real
* Como consumir APIs com React/Next.js
* Como manipular estado e lidar com formulários
* Como organizar um projeto para portfólio

---

