# Desafio BI Alura 2023

Rápida descrição do objetivo de fazer esse projeto

| :placard: Vitrine.Dev |     |
| -------------  | --- |
| :sparkles: Nome        | **TChallenge BI - Semana 1**
| :label: Tecnologias | PowerBi
| :rocket: URL         | https://url-deploy.com.br
| :fire: Desafio     | [https://url-do-desafio.com.br](https://www.alura.com.br/challenges/bi-3/semana-01-analisando-campanha-marketing)

<!-- Inserir imagem com a #vitrinedev ao final do link -->
![Desafio - Semana 1_pages-to-jpg-0001](https://github.com/Jneliorr/Challenge-BI---Semana-1/assets/134644706/3863b57e-587d-4dc2-b4f2-fe7b363eb0ef#vitrinedev)



## Detalhes do projeto

A empresa Bloco de Código precisava de uma analise para monitorar sua campanha de marketing.
Inicialmente comecei realizando ETL dos dados disponibilizados.
Ultilizei 14 medidas em dax para extrair informações gerais.
ultilizando um vizual externo PureViz que gereis card personalizados ultilizando imagens svg criandas no figma

## ETL

**Transformação inicial da Coluna Data**

_= Table.TransformColumnTypes(#"Tipo Alterado", {{"Data", type date}}, "en-US")_
![1](https://github.com/Jneliorr/Challenge-BI---Semana-1/assets/134644706/7525a10e-f732-4ec0-a3f5-ced88c681656)



**Filtro Coluna Article URL**

Um linha embranco pode causar um problema na analise de contagem dos dados

_= Table.SelectRows(#"Tipo Alterado com Localidade", each ([Article URL] <> null and [Article URL] <> ""))_
![2](https://github.com/Jneliorr/Challenge-BI---Semana-1/assets/134644706/222712ce-5a52-4975-9e7a-484a5fb8053e)

