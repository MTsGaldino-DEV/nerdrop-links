# NERD DROP — Bio Link

Página de links (bio-link) do grupo de ofertas **NERD DROP**. Site estático, sem build e sem dependências: um único `index.html` com CSS e JS inline.

## Estrutura

| Arquivo | Função |
| --- | --- |
| `index.html` | A página inteira (HTML + CSS + JS) |
| `assets/mascote.png` / `.webp` | Mascote exibido no topo |
| `assets/logo-completa.png` | Logo com wordmark, fundo transparente (uso avulso) |
| `og.png` | Miniatura ao compartilhar o link (1200x630) |
| `favicon.png`, `apple-touch-icon.png` | Ícones do site |
| `vercel.json` | Configuração de deploy e headers |
| `robots.txt` | Liberação para buscadores |

Todas as imagens foram geradas a partir de `NERD-DROP-transparente.png`.

## Identidade visual aplicada

| Uso | Cor |
| --- | --- |
| Fundo | `#0A0A0A` |
| "NERD" | `#FFFFFF` |
| "DROP" / botão principal | `#FFD62E` |
| Detalhe (status "ativo agora") | `#BEFF00` |
| Contorno do mascote | `#5C1622` |

Tipografia: **Archivo Black** no wordmark e no botão principal, **Inter** no restante. As cores estão nas variáveis CSS no topo do `<style>` (`--amarelo`, `--verde-neon`, `--preto`…) — mudar ali muda a página inteira.

## Como editar

**Link do grupo do WhatsApp** — procure por `chat.whatsapp.com` no `index.html` e troque o `href`.

**Adicionar / remover um link** — duplique um bloco `<a class="link">` dentro de `<nav class="links">` e altere `href`, `.title` e `.sub`. A ordem no HTML é a ordem na tela.

**Instagram e Telegram** estão com links genéricos (`https://www.instagram.com/` e `https://t.me/`) — troque pelos seus perfis ou apague os blocos se não usar.

**Verificação Lomadee** — esta tag precisa continuar no `<head>`; é o que valida o site na plataforma:

```html
<meta name="lomadee" content="2324685" />
```

## Rodar localmente

Abra o `index.html` no navegador ou sirva via HTTP (recomendado, para os caminhos `/assets/` funcionarem):

```bash
npx serve .
```

## Deploy (Vercel)

Repositório: `MTsGaldino-DEV/nerdrop-links`. Todo push na branch `main` publica automaticamente.

Primeira vez:

1. Acesse <https://vercel.com/new> e importe o repositório.
2. Framework Preset: **Other**. Build Command e Output Directory: deixe **em branco** (é site estático).
3. Deploy.

Depois de publicar, troque o domínio nas tags `canonical`, `og:url` e `og:image` do `index.html` pelo endereço final.
