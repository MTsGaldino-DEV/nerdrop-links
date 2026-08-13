# Nerd Drop — Bio Link

Página de links (bio-link) do grupo de ofertas **Nerd Drop**. Site estático, sem build e sem dependências: um único `index.html` com CSS e JS inline.

## Estrutura

| Arquivo | Função |
| --- | --- |
| `index.html` | A página inteira (HTML + CSS + JS) |
| `favicon.svg` | Ícone da aba do navegador |
| `vercel.json` | Configuração de deploy e headers |
| `robots.txt` | Liberação para buscadores |

## Como editar

**Trocar o link do grupo do WhatsApp** — em `index.html`, procure por `chat.whatsapp.com` e troque o `href`.

**Adicionar / remover um link** — duplique um bloco `<a class="link">` dentro de `<nav class="links">` e altere `href`, `.title` e `.sub`. A ordem no HTML é a ordem na tela.

**Instagram e Telegram** estão com links genéricos (`https://www.instagram.com/` e `https://t.me/`) — troque pelos seus perfis ou apague os blocos se não usar.

**Cores** — todas ficam nas variáveis no topo do `<style>` (`--accent`, `--accent-2`, `--bg`).

**Verificação Lomadee** — a tag abaixo precisa continuar no `<head>`; é o que valida o site na plataforma:

```html
<meta name="lomadee" content="2324685" />
```

**Miniatura ao compartilhar** — coloque um `og.png` de 1200x630 na raiz e descomente a linha `og:image` no `<head>`.

## Rodar localmente

Basta abrir o `index.html` no navegador. Ou, para servir via HTTP:

```bash
npx serve .
```

## Deploy (Vercel)

O projeto está ligado ao repositório GitHub `MTsGaldino-DEV/nerdrop-links`. Todo push na branch `main` publica automaticamente.

Primeira vez:

1. Acesse <https://vercel.com/new> e importe o repositório.
2. Framework Preset: **Other**. Build Command e Output Directory: deixe **em branco** (é site estático).
3. Deploy.

Depois de publicar, ajuste o domínio real nas tags `og:url` e `canonical` do `index.html`.
