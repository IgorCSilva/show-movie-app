- Criar projeto:
  `npx create-nuxt-app <project-name>`

- Opções:
  - Programming language: JavaScript
  - Package manager: Npm
  - UI framework: None
  - Nuxt.js modules: Axios
  - Linting tools: ESLint, Prettier
  - Testing framework: Jest
  - Rendering mode: Universal (SSR / SSG)
  - Deployment target: Server (Node.js hosting)
  - Deployment tools: (no option)
  - Continuous Integration: None
  - Version Contrl System: Git

- Executando aplicação:
  `cd movieapp`
  `npm run dev`

- Criando uma página com nome do arquivo about.vue podemos acessá-la pelo caminho /about, sem precisar configurar rota.

- Instalando sass:
  `npm install --save-dev sass sass-loader@10 fibers`

- Criar pasta assets dentro de movieapp.
- Colocando css como global no arquivo nuxt.config.js:
```javascript
css: [
    '@/assets/default.scss'
  ],
```

- Criar pasta layouts e em default.vue colocar:
```vue
<template>
  <div class="app">
    <Nuxt />
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>

<style>

</style>
```

- The Movie Database credentials:
  - api key: b2aa182cd510b3825f0fde874abe09bd
  - api read access token: eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJiMmFhMTgyY2Q1MTBiMzgyNWYwZmRlODc0YWJlMDliZCIsInN1YiI6IjYyZDQzYjkzNzJjMTNlMDA1NDg5ZjFhZCIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.obUGo34MGXw2ufwtVIlp3FhJ7pqWpSTbHENdRtZltB8

- Podemos utilizar o async fetch para buscar dados quando a página estiver pronta:
```vue
async fetch() {
  await this.getMovies()
},
```