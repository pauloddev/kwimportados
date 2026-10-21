# KW Importados: landing page

Site estático (HTML + CSS + JS puro), pronto para GitHub + Vercel. Não precisa de build.

## Para preencher depois do deploy

| O quê | Onde |
|---|---|
| **SITE_URL**: trocar `https://TROCAR-PELO-LINK-DO-VERCEL.vercel.app` pelo link de produção | `index.html` linhas 15, 31, 32, 39, 50, 52, 53, 54 · `robots.txt` linha 6 · `sitemap.xml` linha 5 |
| **Conferir WhatsApp** (44) 99757-8738, tirado da ficha da loja no Google | `index.html`: buscar `5544997578738` (todos os botões) · `404.html` |
| **Conferir horário**: seg a sex 8h às 18h15, sáb 8h às 16h, dom fechado (ficha do Google) | `index.html`: bloco `.hours`, rodapé e JSON-LD `openingHoursSpecification` |
| **og-image.jpg** (1200x630) já gerada com logo + equipe; troque se quiser outra arte | raiz do projeto |
| **Favicons** gerados a partir do logo (`favicon.ico`, `favicon.svg`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`); substitua mantendo os nomes | raiz do projeto |

Dica: no VS Code, "Localizar e substituir em arquivos" (Ctrl+Shift+H) troca a URL em todos os arquivos de uma vez.

## Publicar

1. Suba esta pasta para um repositório no GitHub.
2. No Vercel: Add New > Project > importe o repositório (Framework: **Other**, sem build).
3. Copie o link de produção (`seu-projeto.vercel.app`), troque a SITE_URL (tabela acima), faça commit.
4. Abra `/robots.txt` e `/sitemap.xml` no link de produção e confira a URL.
5. Os links de preview do Vercel ficam com noindex por padrão. Isso é normal: confira tudo no link de produção.

## Google Search Console

1. search.google.com/search-console > Adicionar propriedade > **Prefixo do URL** > cole o link de produção.
2. Verifique pela tag HTML (cole a meta no `<head>` do `index.html`, commit, clique em Verificar).
3. Sitemaps > envie `sitemap.xml`.
4. Inspeção de URL > cole a home > Solicitar indexação.

A indexação depende da avaliação do Google; o site só fica preparado para ela.

## Se conectar um domínio próprio

1. Vercel > Settings > Domains > adicione o domínio e configure o DNS.
2. Defina o domínio como principal e redirecione o `.vercel.app` para ele (301).
3. Troque a SITE_URL de novo para o domínio novo.
4. No Search Console, adicione a nova propriedade, envie o sitemap de novo e solicite indexação.
