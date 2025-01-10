# **MultiTenant Project Management System**

Este é um sistema de gerenciamento de projetos multi-tenant com autenticação e controle de acesso baseado em papéis (RBAC). Ele foi desenvolvido utilizando **Next.js**, **Prisma** e **Auth.js** para fornecer uma experiência robusta e escalável para equipes que gerenciam múltiplos projetos e usuários em diferentes tenants.

## **Funcionalidades**

- **Autenticação com Auth.js**:
  - Suporte para login via provedor externo (Google, Email/Password, etc.).
  - Criação de conta e recuperação de senha.
- **Multi-tenancy**:
  - Sistema multi-tenant, permitindo que múltiplos clientes (tenants) usem a mesma aplicação.
  - Cada tenant possui seu próprio conjunto de dados, como usuários, projetos e tarefas.
- **Controle de Acesso (RBAC)**:
  - Diferentes papéis de usuário, como Admin, Manager e Member.
  - Cada papel tem permissões específicas para acessar e gerenciar dados no sistema.
- **Gerenciamento de Projetos e Tarefas**:

  - Criação, edição e exclusão de projetos.
  - Atribuição de tarefas aos membros da equipe.
  - Filtragem e organização de tarefas por status, prazo, e prioridade.

- **Deploy na Nuvem**:
  - Deploy automático utilizando Vercel (ou outra plataforma de sua escolha).
  - Configuração de variáveis de ambiente no painel de deploy.

---

## **Tecnologias Usadas**

- **Next.js**: Framework React para renderização do lado do servidor e geração de páginas estáticas.
- **TypeScript**: Para tipagem estática e maior segurança no código.
- **Prisma**: ORM para interação com o banco de dados.
- **Auth.js**: Biblioteca para autenticação e gerenciamento de sessões.
- **PostgreSQL**: Banco de dados relacional utilizado para persistência de dados.
- **Tailwind CSS**: Framework CSS para estilização rápida e responsiva.

---

## **Como Executar o Projeto Localmente**

### 1. Clone o Repositório

```
git clone [URL_REPOSITORIO]
cd [NOME_REPOSITORIO]
```

### 2. Instale as Dependências

```
npm install
```

### 3. Configure as Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```
DATABASE_URL=[URL_DO_BANCO_DE_DADOS]
NEXTAUTH_URL=[URL_DO_PROJETO]
```

### 4. Execute as Migrações do Prisma

Para configurar o banco de dados:

```
npx prisma migrate dev
```

### 5. Inicie o Servidor de Desenvolvimento

```
npm run dev
```

O servidor estará disponível em `[URL_SERVIDOR]`.

---

## **Deploy**

Este projeto está configurado para ser facilmente implantado na Vercel. Para fazer o deploy:

1. Crie uma conta na Vercel (se ainda não tiver).
2. Conecte o repositório do GitHub ao painel da Vercel.
3. Configure as variáveis de ambiente no painel da Vercel (como `DATABASE_URL` e `NEXTAUTH_URL`).
4. Realize o deploy.

---

## **Estrutura do Projeto**

```
.
├── components/          # Componentes reutilizáveis da UI
├── app/               # Páginas da aplicação
│   ├── api/             # Endpoints da API
│   ├── auth/            # Páginas de autenticação
│   ├── projects/        # Páginas de gerenciamento de projetos
│   └── tasks/           # Páginas de gerenciamento de tarefas
├── prisma/              # Arquivos do Prisma (schema e migrações)
├── public/              # Arquivos públicos como imagens
├── styles/              # Arquivos de estilo (Tailwind CSS)
├── .env                 # Variáveis de ambiente
├── next.config.js       # Configurações do Next.js
└── package.json         # Dependências e scripts do projeto
```

---

## **Contribuindo**

Se você gostaria de contribuir para este projeto, fique à vontade para abrir um **pull request**. Ao fazer isso, siga estas etapas:

1. Fork o repositório.
2. Crie uma branch para a sua feature (`[CRIAR_BRANCH]`).
3. Faça os commits necessários (`[COMMIT_FEATURE]`).
4. Envie para o repositório (`[ENVIAR_BRANCH]`).
5. Abra um pull request.

---

## **Licença**

Este projeto está licenciado sob a MIT License - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## **Autores**

- **João Victor**: Criador e mantenedor principal do projeto.
