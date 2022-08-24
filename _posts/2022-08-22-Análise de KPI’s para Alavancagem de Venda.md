---
date: 2022-08-22
title: Análise de KPI’s para Alavancagem de Venda
categories:

featured_image: "./images/Análise de KPI’s para Alavancagem de Vendas.jpg"
recipe:
 
---
Para a análise efetuada foram utilizadas os seguintes critérios:

Não foram considerados as linhas em branco.

Subdivisão do banco de dados em dois formatos em M:

Uma Tabela apenas para pedidos e prazos,
E um agrupamento de dados apenas para Soma de valor de frete e valor de produtos por n° do pedido.

Medidas Dax Utilizadas:

DATADIFF / IF/ AN/ ISBLANK / CALCULATE / COUNT.

Data de Envio - Data Limite do envio para saber se o pedido tinha sido enviado no prazo ou não.
Data de Entrega - Data Limite da Entrega para saber se o pedido tinha sido Entregue no prazo ou não.
Se a condição criada anteriormente retornasse BLANK é 0, se retornasse <0 (Números negativos) é 1 e se retornasse >0 é 3.
Com isso consegui montar uma lógica para saber quais data de envio e quais datas de entrega estavam em branco, em atraso ou entregue no prazo.
Fiz uma contagem distinta dos pedidos da base tirando os pedidos duplicados.
E criei  medidas de %  dentro e fora do prazo de entrega e de envio, filtrando condições 1 e 3 criadas anteriormente.
Para os Pedidos Cancelados, todas as linhas que na coluna Status de cancelamento fossem diferente de em branco, foram cancelados.



![](https://github.com/Giovanacarmazio/portifolio/blob/main/images/An%C3%A1lise%20de%20KPI%E2%80%99s%20para%20Alavancagem%20de%20Venda%20-%202.jpg)

![Cupcakes](https://images.unsplash.com/photo-1448131063153-f1e240f98a72?w=1560&h=940&fit=crop)
