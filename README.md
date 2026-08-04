# Fisioterapia Respiratória RJ — Marcus Pereira

Redesenho do site publicado no Canva
(`https://agenciag7pro.my.canva.site/drmarcuspereira`) em HTML/CSS/JS estático,
mantendo **todo o conteúdo, as imagens e as funcionalidades do original**.

## Estrutura

```
site-marcus-pereira/
├── index.html      # página única com todas as seções
├── styles.css      # design system + layout + responsivo
├── script.js       # header fixo, menu mobile, reveal on scroll, marquee
└── assets/         # imagens extraídas do site original
```

## O que foi mantido do original

| Original | Aqui |
|---|---|
| Título "Respire melhor. Movimente-se com mais qualidade de vida." | Hero |
| Parágrafo de apresentação | Hero |
| Botão "AGENDAR AVALIAÇÃO" → `https://w.app/pjyost` | Header, hero, CTA final, botão flutuante |
| Serviços: Fisioterapia Respiratória / Cardíaca / Saúde do Idoso | Seção "Serviços" |
| "Como funciona nosso acompanhamento?" (3 etapas) | Seção "Método" |
| "Recursos de Alta Tecnologia" (espirometria, PowerBreathe K5, estrutura) | Seção "Estrutura" |
| 3 perguntas frequentes | Acordeão de FAQ |
| "Estamos prontos para cuidar de você." + e-mail | Seção de CTA |
| Endereço em Copacabana | Rodapé |
| Logo, selo circular e todas as fotos | `assets/` |

> A foto do hero (`hero-jaleco.png` / `.webp`) foi refeita a partir do original
> em alta resolução enviado pelo cliente, com o fundo removido via framework
> Vision do macOS. A versão que vinha do Canva era baixa e cortava o topo da
> cabeça. O `<picture>` serve WebP (~124 KB) e cai para PNG onde não houver suporte.

## O que mudou (melhorias)

- **Identidade tipográfica**: Newsreader (display, editorial) + Archivo (texto),
  no lugar das fontes genéricas do Canva.
- **Paleta ampliada** a partir das cores originais (`#1b7173`, `#2fdbbc`, `#c5ffbc`),
  com fundo papel quente e seções escuras para criar ritmo.
- **Navegação real** com header fixo, âncoras e menu mobile — o original era
  uma página sem navegação.
- **Responsivo de verdade** (o Canva entrega um canvas de 1366px escalado).
- **Acessibilidade**: HTML semântico, `skip link`, foco visível, `alt` descritivo
  em todas as imagens, acordeão nativo (`<details>`), suporte a
  `prefers-reduced-motion`.
- **SEO**: meta description, Open Graph, e JSON-LD `MedicalBusiness` com
  endereço e serviços.
- **Micro-interações**: reveal no scroll, selo girando, anéis de "respiração"
  no hero, faixa deslizante, hover nos cards.
- **Botão flutuante de WhatsApp** que aparece após o hero.

### Textos novos (curtos)

Os cards de serviço no original tinham só o título. Foram acrescentadas
uma linha de apoio em cada um, escrita a partir do vocabulário já presente
no site (check-up respiratório, pós-operatório, consultório e domicílio).
Se preferir manter só os títulos, é só apagar o `<p>` dentro de `.card-body`.

## Como rodar

Abra `index.html` no navegador. Não há build nem dependências.
As fontes vêm do Google Fonts (precisa de internet); o resto é local.

## Publicar

Qualquer host estático serve — Vercel, Netlify, GitHub Pages, Cloudflare Pages.
Basta subir a pasta inteira.

Antes de publicar, ajustar em `index.html`:
- `<link rel="canonical">` para o domínio final;
- `og:image` para a URL absoluta da imagem.
