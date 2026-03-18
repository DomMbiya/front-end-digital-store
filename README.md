# Loja Drip (React + Vite)

Aplicação de e-commerce front-end desenvolvida com React, Vite e Tailwind CSS, focada em navegação de produtos, carrinho persistente e fluxo de compra de um catálogo de moda urbana.

---

## 🚀 Tecnologias

- React 19 + React Router DOM 7
- Vite 7
- Tailwind CSS v4 com plugin `@tailwindcss/postcss`
- PostCSS + Autoprefixer
- ESLint com regras básicas `@eslint/js` + React hooks
- Axios (para simular chamadas de API / integração futura)

## ✨ Funcionalidades principais

- Página inicial com hero, coleções em destaque e filtro por categoria
- Listagem de produtos (`/produtos`) com:
  - busca por query
  - filtro por marca, categoria, gênero e estado
  - ordenação por preço (menor / maior)
- Página de produto detalhado (`/produto/:id`) com imagens, descrição e relacionados
- Carrinho de compras com persistência (`localStorage`): adicionar, remover, limpar
- Autenticação básica (páginas `login`, `register`, `completar-cadastro`)
- Página de pedidos (`/pedidos`)

## 📁 Estrutura do projeto

- `src/App.jsx` - configuração de rotas
- `src/pages` - páginas da aplicação
- `src/components` - componentes UI e layout
- `src/contexts/cartContext.jsx` - contexto do carrinho
- `src/data/products.js` - catálogo de produtos fictício
- `src/services/api.js` - wrapper para chamadas de API
- `src/index.css` - import Tailwind + variáveis CSS

## ▶️ Como rodar

1. clonar repo

```bash
git clone <repo-url>
cd loja-drip
```

2. instalar dependências

```bash
npm install
```

3. rodar modo dev

```bash
npm run dev
```

Acesse: `http://localhost:5173`

## 🛠️ Scripts úteis

- `npm run dev` - desenvolvimento com HMR
- `npm run build` - build de produção
- `npm run preview` - preview do build
- `npm run lint` - verificação de lint

## 🌱 Melhorias futuras

- backend real + API REST
- autenticação JWT + confirmação de e-mail
- checkout e cálculo de frete
- testes unitários e E2E
- otimização de performance e imagem lazyload

## 💡 Observações

- Rota `produtos?categoria=<nome>` inicializa filtro por categoria.
- `CartProvider` deve envolver o app para persistência de carrinho.
- `useMemo` é usado no filtro de produtos para performance.

