---
date: 2017-01-07
title: Análise de KPI’s para Alavancagem de Venda
categories:
portifolio
featured_image: "./images/Análise de KPI’s para Alavancagem de Vendas.jpg"
recipe:
  servings: 12 cupcakes
  prep: 5 minutes
  cook: 25 minutes
  ingredients_markdown: |-
    **Cupcakes**

    * 2 cups flour
    * 1/2 cup cocoa powder
    * 1 tablespoon baking powder
    * 1 tsp. salt
    * 1/2 tsp. baking soda
    * 4 tablespoons butter
    * 4 oz. applesauce
    * 1 cup sugar
    * 2 eggs
    * 4 oz. chocolate
    * 1 tsp. vanilla
    * 1/2 cup whole milk
    * 1/2 cup boiling water

    **Icing**

    * 8 oz. of cream cheese
    * 1 cup of powdered sugar
    * 1/4 cup milk
    * 1 tablespoon butter
  directions_markdown: |-
    **Cupcakes**

    1. Preheat Oven 350 degree
    2. In a bowl combine flour, cocoa baking powder, baking soda and salt.
    3. In a food processor combine butter and sugar and process until smooth. Add the eggs, 4 oz. of chocolate pieces and vanilla. Add half of the flour mixture and ½ of the milk. Process and add the other half of the flour and the remainder of the milk. Slowly, add the hot water.
    4. Grease and fill muffin tins to top.
    5. Bake 20 25 minutes or until toothpick test comes out clean.
    6. Let cool.

    **Icing**
    1. Combine all of the above in a food processor and process until smooth. Refrigerate.
    2. Frost cupcakes as you use them.
---
These chocolate chocolate cupcakes have a stunning appearance and a rich, chocolatey sweetness. I've found at parties people prefer bite sized deserts so I'd recommend making 24 mini cupcakes rather than 12 large. That way you won't find half eaten cupcakes at your party!

![Cupcakes](https://images.unsplash.com/photo-1448131063153-f1e240f98a72?w=1560&h=940&fit=crop)

![Cupcakes](https://images.unsplash.com/photo-1420730614543-e39f93134b0d?w=1560&h=940&fit=crop)

![Cupcakes](https://images.unsplash.com/photo-1457508252818-162dc1934c2f?w=1560&h=940&fit=crop)





  
featured_image: 


##Critérios Utilizados na Análise

#####Para a análise efetuada foram utilizadas os seguintes critérios:

Não foram considerados as linhas em branco.

Subdivisão do banco de dados em dois formatos em M:

Uma Tabela apenas para pedidos e prazos,

E um agrupamento de dados apenas para Soma de valor de frete e valor de produtos por n° do pedido.

#####Medidas Dax Utilizadas:

DATADIFF / IF/ AN/ ISBLANK / CALCULATE / COUNT.

Data de Envio - Data Limite do envio para saber se o pedido tinha sido enviado no prazo ou não.
Data de Entrega - Data Limite da Entrega para saber se o pedido tinha sido Entregue no prazo ou não.
Se a condição criada anteriormente retornasse BLANK é 0, se retornasse <0 (Números negativos) é 1 e se retornasse >0 é 3.
Com isso consegui montar uma lógica para saber quais data de envio e quais datas de entrega estavam em branco, em atraso ou entregue no prazo.
Fiz uma contagem distinta dos pedidos da base tirando os pedidos duplicados.
E criei  medidas de %  dentro e fora do prazo de entrega e de envio, filtrando condições 1 e 3 criadas anteriormente.
Para os Pedidos Cancelados, todas as linhas que na coluna Status de cancelamento fossem diferente de em branco, foram cancelados.

![](images/Análise de KPI’s para Alavancagem de Venda - 2.jpg)


![](images/Análise de KPI’s para Alavancagem de Venda - 3.jpg)
