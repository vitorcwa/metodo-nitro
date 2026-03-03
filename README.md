# CWA Digital — Landing Page

Projeto Vue 3 + Vite. Pronto para deploy em Vercel ou Netlify.

---

## 🚀 Rodando localmente

```bash
# 1. Instalar dependências
npm install

# 2. Iniciar servidor de desenvolvimento
npm run dev
```

Abra http://localhost:5173

---

## 🖼️ Logo

Coloque o arquivo da logo CWA em:

```
/public/logo-cwa.png
```

---

## 📦 Build de produção

```bash
npm run build
```

Os arquivos ficam em `/dist` — é essa pasta que vai para o deploy.

---

## ☁️ Deploy na Vercel (recomendado)

1. Instale a CLI: `npm i -g vercel`
2. Na raiz do projeto: `vercel`
3. Siga o assistente — o Vite é detectado automaticamente
4. Para deploys futuros: `vercel --prod`

**Ou via painel:**
- Acesse vercel.com → New Project → importe o repositório
- Framework: **Vite** (detectado automaticamente)
- Build command: `npm run build`
- Output dir: `dist`
- Clique Deploy ✓

---

## ☁️ Deploy na Netlify

**Via painel:**
- Acesse netlify.com → Add new site → Import from Git
- Build command: `npm run build`
- Publish directory: `dist`
- Clique Deploy ✓

**Ou via CLI:**
```bash
npm i -g netlify-cli
netlify deploy --prod --dir=dist
```

Crie um arquivo `netlify.toml` na raiz (já incluído):

```toml
[build]
  command = "npm run build"
  publish = "dist"
```

---

## 📁 Estrutura do projeto

```
cwa-landing/
├── public/
│   └── logo-cwa.png          ← coloque a logo aqui
├── src/
│   ├── assets/
│   │   └── global.css         ← tokens de design e estilos globais
│   ├── composables/
│   │   └── useScrollReveal.js ← animações de scroll
│   ├── components/
│   │   ├── NavBar.vue
│   │   ├── HeroSection.vue
│   │   ├── LogosBand.vue
│   │   ├── QuemSomos.vue
│   │   ├── ProblemaSection.vue
│   │   ├── MetodoNitro.vue
│   │   ├── FunilSection.vue
│   │   ├── PdiSection.vue
│   │   ├── TreinamentosSection.vue
│   │   ├── ResultadosSection.vue
│   │   ├── GrandeQuote.vue
│   │   ├── PlanoSection.vue
│   │   ├── DepoimentosSection.vue
│   │   ├── FaqSection.vue
│   │   ├── CtaSection.vue
│   │   └── FooterSection.vue
│   ├── App.vue
│   └── main.js
├── index.html
├── vite.config.js
├── package.json
└── netlify.toml
```

---

## ✏️ Customizações comuns

| O que mudar | Onde |
|---|---|
| Links WhatsApp / redes sociais | `FooterSection.vue` e `CtaSection.vue` |
| Depoimentos reais de clientes | `DepoimentosSection.vue` |
| Cores e fontes | `src/assets/global.css` → `:root {}` |
| Textos e copy | Cada componente `.vue` |
| Logo | `public/logo-cwa.png` |
