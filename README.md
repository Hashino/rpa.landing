# Soluções RPA — Landing Page

Landing page estática (HTML + CSS + JS puro), sem back-end e sem build. Basta hospedar os 3 arquivos:

- `index.html`
- `styles.css`
- `script.js`

## Antes de publicar — personalize

Procure e ajuste no `index.html`:

1. **E-mail de contato**: `contato@solucoesrpa.com.br` (seção Contato) — troque pelo e-mail real.
2. **WhatsApp**: o link `https://wa.me/5500000000000` — troque pelo número real no formato `55` + DDD + número (só dígitos).
3. **Domínio nos metadados**: se quiser, adicione `<link rel="canonical">` e Open Graph com o domínio final.

## Como publicar (grátis)

Qualquer hospedagem estática funciona. Duas opções simples:

### Cloudflare Pages (recomendado)
1. Crie uma conta em [pages.cloudflare.com](https://pages.cloudflare.com).
2. Faça upload direto da pasta (ou conecte um repositório Git).
3. Em **Custom domains**, adicione seu domínio.
4. No registro.br, em **DNS → Alterar servidores DNS**, aponte para os nameservers que a Cloudflare indicar (ou crie um CNAME se preferir manter o DNS no registro.br).

### GitHub Pages
1. Crie um repositório e suba os arquivos.
2. Em **Settings → Pages**, ative o Pages na branch principal.
3. Em **Custom domain**, informe seu domínio.
4. No painel DNS do registro.br, crie os registros `A` apontando para os IPs do GitHub Pages (185.199.108.153, .109., .110., .111.) e um `CNAME` de `www` para `<seu-usuario>.github.io`.

A propagação de DNS pode levar de alguns minutos a 24h.

## Teste local

Abra o `index.html` direto no navegador, ou rode:

```bash
python -m http.server 8000
# http://localhost:8000
```
