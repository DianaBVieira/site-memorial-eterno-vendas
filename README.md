# Memorial Eterno — Página de vendas

Landing page estática (um único `index.html`, sem build) da solução
**Memorial Eterno** da [Utopia Desenvolvimentos](https://www.utopiadesenvolvimentos.com.br).

Memorial digital com QR Code: biografia, galeria de fotos e vídeos, mural de
homenagens e placa personalizada (porcelana ou inox) para a lápide.

## Como ver localmente

```bash
python -m http.server 8140 --bind 127.0.0.1
# depois acesse http://localhost:8140
```

## Estrutura

- `index.html` — página inteira, CSS e JS embutidos
- `assets/` — imagens otimizadas + `favicon.svg`
- `robots.txt`, `sitemap.xml`, `.nojekyll` — publicação / SEO

## SEO

- `<title>`, meta description e keywords focados em: memorial digital, memorial
  com QR Code, QR Code para lápide, homenagem póstuma, placa memorial personalizada
- Open Graph + Twitter Card (`assets/og.jpg`)
- JSON-LD: `Organization`, `Product` (com `AggregateOffer`) e `FAQPage`
- `sitemap.xml` e `robots.txt`

## Deploy

Qualquer host estático serve (GitHub Pages, Firebase Hosting, Cloudflare Pages,
Netlify). O domínio pretendido é `vendasmemorialeterno.utopiadesenvolvimentos.com.br` — ao
definir, atualizar as URLs `canonical`/OG no `index.html`, o `sitemap.xml` e o
`robots.txt`, e adicionar um arquivo `CNAME` se for GitHub Pages.

## Origem do conteúdo

Copy e imagens adaptados da versão em `vinext` criada anteriormente
(`Modelos_de_Servico_UtopiaDesenvolvimentos/Pagina_vendas_individual/Memorial_Eterno_pagina`),
convertida para HTML estático para carregamento rápido e melhor indexação.
