<div align="center">

# 🎮 PlataformaDCC

**Catálogo curado de jogos educacionais para o ensino de Computação**

[![Plataforma](https://img.shields.io/badge/Acessar%20Plataforma-plataforma--dcc.vercel.app-6366f1?style=for-the-badge&logo=vercel&logoColor=white)](https://plataforma-dcc.vercel.app/)
[![Repositório Starter](https://img.shields.io/badge/Repositório%20Dev-plataformadcc--dev-0ea5e9?style=for-the-badge&logo=github&logoColor=white)](https://github.com/plataformadcc/plataformadcc-dev)
[![Licença](https://img.shields.io/badge/Licença-MIT-22c55e?style=for-the-badge)](LICENSE)

</div>

---

## Sobre o projeto

A **PlataformaDCC** é uma plataforma web de jogos educacionais desenvolvida para apoiar o ensino de Computação. Ela reúne jogos em um catálogo curado, com foco em qualidade pedagógica, segurança e acessibilidade para diferentes faixas etárias.

Cada jogo passa por um processo de curadoria antes de ser publicado. A plataforma conta com controle parental, área de desenvolvedor e painel administrativo — tudo em um sistema integrado.

---

## ✨ Funcionalidades

| Funcionalidade | Descrição |
|---|---|
| 🎮 Catálogo de jogos | Listagem com filtros por categoria e classificação indicativa |
| 🔒 Controle parental | Perfis infantis com bloqueio por jogo e tempo de sessão |
| 👨‍💻 Área do desenvolvedor | Submissão e acompanhamento de jogos para curadoria |
| 🌐 Multilíngue | Interface em pt-BR e es |
| 📱 Responsivo | Jogos adaptados para desktop e mobile |

---

## 🛠️ Tecnologias

<div align="center">

![Nuxt 3](https://img.shields.io/badge/Nuxt%203-00DC82?style=for-the-badge&logo=nuxt.js&logoColor=white)
![Vue 3](https://img.shields.io/badge/Vue%203-42b883?style=for-the-badge&logo=vue.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178c6?style=for-the-badge&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind%20CSS-06b6d4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![PrimeVue](https://img.shields.io/badge/PrimeVue-4-7c3aed?style=for-the-badge&logo=primevue&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

</div>

---

## 🚀 Como contribuir com um jogo

Quer publicar um jogo na plataforma? O processo é simples:

### 1. Clone o repositório de desenvolvimento

```bash
git clone https://github.com/plataformadcc/plataformadcc-dev.git
cd plataformadcc-dev
npm install
npm run dev
```

### 2. Adicione seu jogo

Crie a pasta do seu jogo seguindo o contrato esperado:

```
public/_games/
└── meu-jogo/
    ├── index.html      ← entrypoint obrigatório
    └── assets/         ← CSS, JS, imagens, fontes
```

Registre o jogo no catálogo local (`games.config.ts`) e teste localmente em `http://localhost:3000/games/meu-jogo`.

### 3. Valide antes de submeter

- [ ] `index.html` funciona como entrypoint sem dependências externas críticas
- [ ] Sem coleta de dados pessoais ou rastreadores
- [ ] Sem redirecionamentos que quebrem a navegação da plataforma
- [ ] Funciona corretamente em iframe sandbox
- [ ] Objetivo educacional claro e classificação indicativa coerente

### 4. Submeta para curadoria

Acesse a [plataforma](https://plataforma-dcc.vercel.app/), crie uma conta como desenvolvedor e envie seu jogo pelo painel. Ele passará por curadoria técnica e pedagógica antes de ser publicado.

---

## 🗂️ Repositórios

| Repositório | Descrição |
|---|---|
| [`plataformadcc`](https://github.com/plataformadcc) | Perfil do github da plataforma |
| [`plataformadcc-dev`](https://github.com/plataformadcc/plataformadcc-dev) | Starter para desenvolvedores testarem jogos localmente |

---

## 🎯 Arquitetura dos jogos

Os jogos são **builds estáticos** executados em **iframe sandbox**, isolados do restante da plataforma. O contrato é simples: uma pasta com `index.html` como ponto de entrada.

```
Plataforma (Nuxt 3)
└── /games/[slug]
    └── <iframe src="/_games/[slug]/index.html" sandbox="..." />
```

Isso garante que qualquer jogo feito em HTML/CSS/JS puro, Canvas, ou qualquer framework que gere build estático funciona sem adaptações.

---

<div align="center">

Feito com 💙 para o ensino de Computação

</div>
