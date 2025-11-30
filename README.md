**IgNews**

Projeto exemplo de uma aplicação de notícias construída com Next.js. O objetivo deste repositório é demonstrar uma integração com Prismic (CMS), FaunaDB e Stripe para gerenciamento de conteúdos, autenticação e assinaturas.

**Tecnologias**
- **Next.js**: Framework React para SSR/SSG.
- **React**: Biblioteca de UI.
- **Prismic**: CMS usado para gerenciar publicações.
- **FaunaDB**: Banco de dados serverless para assinaturas/usuários.
- **Stripe**: Pagamentos e gerenciamento de assinaturas.
- **TypeScript**: Tipagem estática.

**Pré-requisitos**
- **Node.js** (recomendado 16+)
- **Yarn** ou **npm**
- Contas/configurações no Prismic, FaunaDB e Stripe (para chaves de API)

**Instalação**
1. Clone o repositório:

```fish
git clone https://github.com/AlanJhonatan/ignews.git
cd ignews
```

2. Instale as dependências com `npm` ou `yarn`:

```fish
# usando npm
npm install

# ou usando yarn
yarn
```

**Variáveis de ambiente**
Crie um arquivo `.env.local` na raiz com as chaves necessárias. Exemplo mínimo (substitua pelos seus valores reais):

```
# Prismic
PRISMIC_ENDPOINT=https://your-repo-name.cdn.prismic.io/api/v2
PRISMIC_ACCESS_TOKEN=

# FaunaDB
FAUNADB_SECRET=your_fauna_secret

# Stripe
STRIPE_SECRET_KEY=sk_live_...
STRIPE_PUBLIC_KEY=pk_live_...
WEBHOOK_SECRET=whsec_...

# NextAuth / Autenticação
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=algum_segredo_complexo
```

Observação: dependências específicas de variáveis podem estar nos arquivos dentro de `src/pages/api` e nos serviços em `src/services`.

**Scripts úteis**
- **dev**: roda o servidor em modo desenvolvimento (`next dev`).
- **build**: cria a versão de produção (`next build`).
- **start**: inicia a aplicação em produção (`next start`).
- **lint**: roda o linter (`next lint`).
- **slicemachine**: inicia a Slice Machine (Prismic Slice Library UI).

Comandos:

```fish
# rodar em desenvolvimento
npm run dev

# build para produção
npm run build

# iniciar servidor em produção (após build)
npm start

# rodar slice machine (Se estiver usando Slices do Prismic)
npm run slicemachine
```

**Estrutura do projeto (resumido)**
- **`src/pages`**: rotas e APIs do Next.js (`/pages/api` contém endpoints como `subscribe`, `webhooks`, e autenticação em `auth/[...nextauth].ts`).
- **`src/components`**: componentes React reutilizáveis (ex.: `Header`, `SignInButton`, `SubscribeButton`).
- **`src/services`**: wrappers para integração com APIs externas (Prismic, Fauna, Stripe, etc.).
- **`public`**: arquivos estáticos.

**Notas sobre a implementação**
- A aplicação integra `Prismic` para o conteúdo das postagens.
- `FaunaDB` é utilizado para controlar assinaturas/usuários; confira `src/services/fauna.ts` e `src/pages/api/_lib/manageSubscription.ts`.
- `Stripe` é usado para criar checkout de assinaturas e para tratar webhooks; ver `src/services/stripe.ts` e `src/pages/api/webhooks.ts`.

**Contribuindo**
- Abra um issue para discutir mudanças maiores.
- Faça forks/branches para mudanças e envie pull requests com descrições claras.

**Testes**
Este repositório não possui uma suíte de testes configurada (por padrão). Recomenda-se adicionar testes unitários (Jest/React Testing Library) se for estender o projeto.

**Licença**
O repositório não contém um arquivo de licença por padrão. Adicione um `LICENSE` se for compartilhar publicamente com termos específicos.

**Contato**
Se precisar de ajuda com o projeto, abra uma issue no repositório ou entre em contato com o autor/maintainer.

---

Arquivo criado automaticamente: `README.md` (Português).
