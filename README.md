# Portfólio de Análise de Dados — Daniel de Carvalho Nunes

Site pessoal publicado com GitHub Pages.

- **Página inicial:** https://danicarvalho-1995.github.io/
- **Projeto Nara Hotéis:** https://danicarvalho-1995.github.io/nara-hoteis.html
- **Repositório do portfólio:** https://github.com/danicarvalho-1995/danicarvalho-1995.github.io
- **Projeto-fonte:** https://github.com/danicarvalho-1995/Nara-Hoteis

## Estrutura do site

- `index.html`: apresentação profissional, competências e acesso ao projeto em destaque.
- `nara-hoteis.html`: dashboard web interativo do projeto Nara Hotéis, com filtros por região, ano e unidade; indicadores, gráficos e explicações metodológicas.
- `nara-data.js`: agregações mensais derivadas das bases limpas do projeto. Contém somente contagens de reservas e hóspedes por mês, região e unidade; não contém nomes, identificadores de clientes ou registros individuais.
- `.github/workflows/pages.yml`: publicação automática no GitHub Pages após alterações na branch `main`.

## Dashboard Nara Hotéis

A página web foi recriada a partir da estrutura visual e dos campos identificados no arquivo `Nara Hoteis.pbix`. A reprodução contempla:

1. Filtro regional.
2. Gráfico combinado de total de hóspedes e média de hóspedes por reserva por unidade.
3. Série temporal de reservas por mês e região.
4. Tabela comparativa com reservas do mês, mês anterior, variação mensal e mesmo mês do ano anterior.
5. Explicações de cada visual, medidas e cuidados de interpretação.

Os filtros por ano e unidade foram acrescentados para facilitar a exploração na página web. Eles atualizam os indicadores, os gráficos e a tabela em conjunto.

## Dados e metodologia

As agregações web são derivadas de:

- `reservaslimpo.csv`
- `unidadeslimpo.csv`

Na versão consultada, a base contém 4.649 registros de reservas, 13 unidades e check-ins entre janeiro de 2023 e agosto de 2026.

O arquivo `nara-data.js` reúne 547 agregações no grão mês de check-in × região × unidade. Ele é gerado sem dados pessoais de clientes. A soma de hóspedes representa o total informado nos registros de reservas, não pessoas únicas. A contagem de reservas considera todos os status, pois o painel do PBIX não apresenta filtro de status nesta página.

Há duas variações de capitalização no campo de região para “Baixada Fluminense”. Na experiência web, esses valores foram agrupados sob o mesmo rótulo para evitar duplicidade visual. Os demais rótulos foram preservados.

**Importante:** a página web é uma reprodução interativa independente, em HTML, CSS e JavaScript. Ela não executa o arquivo PBIX nem incorpora o motor do Power BI. Os gráficos são recalculados a partir das agregações disponibilizadas no próprio site.

## Publicação

O workflow em `.github/workflows/pages.yml` publica os arquivos estáticos após um push para a branch `main`. A configuração do Pages deve usar **GitHub Actions** como fonte de publicação.

## Autoria

Portfólio de Daniel de Carvalho Nunes. O projeto Nara Hotéis foi desenvolvido por Daniel de Carvalho Nunes e Karoline Duffrayer.

## Contexto externo do mercado hoteleiro

A página `nara-hoteis.html` contém uma seção com seis reportagens autorizadas para contextualizar as análises do projeto: O Globo (Rock in Rio), Folha de S.Paulo (Lady Gaga em Copacabana e cenário do turismo doméstico), UOL (Réveillon no Rio e NFL no Rio) e Metrópoles (hotelaria de luxo).

Essas matérias são referências externas do mercado real. Seus indicadores não são misturados aos dados da rede fictícia Nara Hotéis nem incorporados aos cálculos e gráficos do dashboard. As prévias de ocupação, resultados de eventos, médias nacionais e dados de hotelaria de luxo possuem escopos distintos e devem ser comparados com cautela.
