# CLAUDE.md — QUEROSERSF

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** QUEROSERSF
**Nicho:** Negócios e Empreendedorismo
**Keywords:** A QUEROSERSF e a casa do seu trabalho Nossa missao e fornecer
**Paleta de cores:** sunset | **Fonte:** playfair

A QUEROSERSF é a casa do seu trabalho. Nossa missão é fornecer a você um espaço onde você possa ser produtivo e criativo. Acreditamos que quando você tem um ambiente que suporta sua produtividade, você é capaz de alcançar coisas incríveis. Oferecemos uma variedade de serviços para ajudá-lo a obter o máximo do seu trabalho, incluindo espaços para coworking, salas de reunião e espaço para eventos. Também oferecemos serviços de escritório virtual, que lhe permitem ter uma presença profissional sem ter que se preocupar com as operações do dia-a-dia de um escritório físico. Nossa equipe é dedicada a ajudá-lo a ter sucesso, e estamos sempre procurando novas maneiras de melhorar nossos serviços. Se houver algo que possamos fazer para ajudar a fazer seu trabalho melhor, pode contar com a gente!



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-D |
| Hero | Hero-B |
| Features | Features-C |
| About Section | About-G |
| Posts | Posts-H |
| Footer | Footer-A |
| Página Sobre | Sobre-G |
| Página Contato | Contato-F |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
