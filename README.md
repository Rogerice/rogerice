# Site — Rogério Rodrigues

Site profissional de apresentação (portfólio), construído com **React + Vite + TailwindCSS** e animações com **Framer Motion**.

A estratégia do site: **primeiro vender o profissional** (autoridade, trajetória e especialidades) e **depois mostrar os projetos** como prova concreta da experiência.

## Como rodar localmente

> O `npm` via PowerShell pode estar bloqueado por política de execução. Use `npm.cmd` no Windows.

```bash
npm.cmd install
npm.cmd run dev
```

O site abre em `http://localhost:5173`.

## Build de produção

```bash
npm.cmd run build
npm.cmd run preview
```

Os arquivos finais ficam na pasta `dist/`.

## Estrutura

```
src/
  data/content.js      <- TODO o conteúdo editável (textos, marcas, projetos, contatos)
  components/          <- Seções do site (Hero, About, Trajectory, ...)
  App.jsx              <- Ordem das seções
  index.css            <- Tema, cores e fontes
public/favicon.svg     <- Ícone do site
```

## O que personalizar (em `src/data/content.js`)

- **`contact`** — troque os placeholders pelos seus dados reais:
  - `email`, `whatsapp` (formato `5511999999999`), `linkedin`, `github`.
- **`profile`**, **`about`**, **`trajectory`**, **`projects`**, **`personal`** — ajuste os textos.
- **Foto**: o componente `src/components/About.jsx` tem um espaço reservado para sua foto.

## Publicar na Netlify

1. Suba o projeto para um repositório no GitHub.
2. No painel da Netlify: **Add new site → Import an existing project** e selecione o repositório.
3. A Netlify lê o `netlify.toml` automaticamente:
   - Build command: `npm run build`
   - Publish directory: `dist`
4. Deploy. Pronto — cada `git push` atualiza o site.

Alternativa rápida sem Git: `npm.cmd run build` e arraste a pasta `dist/` em https://app.netlify.com/drop
