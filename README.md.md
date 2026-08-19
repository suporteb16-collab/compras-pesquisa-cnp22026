# Relatório de Compradores — Mundial Cromo CNP2 2026

Relatório estático e compartilhável da **Pesquisa de Compradores** do lançamento CNP2 2026, com aba de comparação contra a **Pesquisa de Captação**.

## O que é

Um único arquivo `index.html`, autônomo (dados embutidos no próprio HTML). **Não se conecta a nenhuma planilha** nem ao dashboard ao vivo — é uma fotografia do lançamento, pensada para enviar a outras pessoas.

- **Paleta:** design system B16 (fundo `#F4F4F2`, dourado `#D4A800`, preto `#111`, fontes Bebas Neue + DM Sans).
- **Dependência externa:** Chart.js 4.4.1 via CDN (Cloudflare). Se o CDN falhar, os gráficos exibem aviso e o resto do relatório continua funcionando.

## Abas

1. **Pesquisa de Compradores** — KPIs do lançamento, curva de vendas por dia, perfil do comprador (idade, renda, canal, tempo de acompanhamento, conhecimento, ocupação), origem do tráfego e motivação.
2. **Compradores × Captação** — perfil de quem comprou vs. toda a base de leads, **índice de conversão por segmento** (quais perfis convertem acima/abaixo da média) e insights acionáveis.

## Regras e tratamento aplicados

- **Comprador = tem data de compra.** Respostas sem `Data Compra` foram descartadas (não compraram no lançamento).
- **Deduplicação:** e-mails repetidos com mesma data e mesmo valor foram consolidados em 1 comprador (respostas duplicadas da mesma compra).
- **Captação — correção de colunas:** a base de captação continha dois formatos de formulário com ordem de colunas diferente (4.644 de 18.032 respostas estavam deslocadas). Cada conceito foi remapeado para a coluna correta antes de comparar. Após a correção, todos os campos ficam 100% dentro do domínio esperado.
- **Índice de conversão** = participação do segmento entre compradores ÷ participação do mesmo segmento entre leads. `1,0` = converte na média; acima = converte mais; abaixo = converte menos.

## Números-chave

- 328 compradores únicos (de 367 respostas com compra) · 18.032 leads
- Faturamento na janela: R$ 213.192 · ticket médio R$ 650 (mediana R$ 683)
- Conversão da base: 1,82%
- Janela de compras: 10 a 18/08/2026

## Publicar no GitHub Pages (mesmo repositório)

Este relatório **não substitui** o dashboard ao vivo nem a planilha. Para hospedar sem conflito, suba em uma **subpasta** do repo `dashboard-b16`:

1. Crie a pasta `compradores-cnp2/` na raiz do repositório.
2. Suba este arquivo como `compradores-cnp2/index.html`.
3. Com o GitHub Pages já ativo no repo, o relatório fica em:
   `https://henriquecardosos96.github.io/dashboard-b16/compradores-cnp2/`

> Assim o dashboard principal (`/`) continua intacto e o relatório ganha um endereço próprio para compartilhar.
