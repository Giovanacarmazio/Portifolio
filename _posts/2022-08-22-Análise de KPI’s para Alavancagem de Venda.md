---
date: 2022-08-22
title: Análise de KPI’s para Alavancagem de Venda
categories:

featured_image: "https://raw.githubusercontent.com/Giovanacarmazio/portifolio/main/images/An%C3%A1lise%20de%20KPI%E2%80%99s%20para%20Alavancagem%20de%20Vendas.jpg"
recipe:
 
---


Análise de KPI’s para Alavancagem de Venda | Medidas Dax Utilizadas: DATADIFF / IF/ AN/ ISBLANK / CALCULATE / COUNT.
![](https://raw.githubusercontent.com/Giovanacarmazio/portifolio/main/images/An%C3%A1lise%20de%20KPI%E2%80%99s%20para%20Alavancagem%20de%20Venda%20-%202.jpg)
![](https://raw.githubusercontent.com/Giovanacarmazio/portifolio/main/images/An%C3%A1lise%20de%20KPI%E2%80%99s%20para%20Alavancagem%20de%20Venda%20-%203.jpg)

Critérios de Análises:


Não foram considerados as linhas em branco.
Subdivisão do banco de dados em dois formatos em M:
Uma Tabela apenas para pedidos e prazos,
E um agrupamento de dados apenas para Soma de valor de frete e valor de produtos por n° do pedido.


Medidas Dax Utilizadas:
<b>DATADIFF / IF/ AN/ ISBLANK / CALCULATE / COUNT.</b>

Data de Envio - Data Limite do envio para saber se o pedido tinha sido enviado no prazo ou não.
Data de Entrega - Data Limite da Entrega para saber se o pedido tinha sido Entregue no prazo ou não.
Se a condição criada anteriormente retornasse BLANK é 0, se retornasse <0 (Números negativos) é 1 e se retornasse >0 é 3.
Com isso consegui montar uma lógica para saber quais data de envio e quais datas de entrega estavam em branco, em atraso ou entregue no prazo.
Fiz uma contagem distinta dos pedidos da base tirando os pedidos duplicados.
E criei  medidas de %  dentro e fora do prazo de entrega e de envio, filtrando condições 1 e 3 criadas anteriormente.
Para os Pedidos Cancelados, todas as linhas que na coluna Status de cancelamento fossem diferente de em branco, foram cancelados.


<b>Análises</b>


Mari Eletro
Está dentro do esperado entre a data de entregas e data de envio.
Dos pedidos cancelados, o valor do frete e o valor dos produtos não apresentam um desvio padrão em relação a venda total. De 1565 pedidos realizados em todos os canais, 1399 são do mercado livre, onde 91 foram cancelados ou suspensos ( 6,5%). 


Lojão Utilidades LTDA
De 485 pedidos recebidos, 28 foram cancelados ou suspensos (5,8%). Dos 28, 20 foram cancelados pelo canal do mercado livre no dia 08/10. Não houveram data de envio e nem data de entrega dos 20 pedidos mencionados anteriormente. Analisando o valor do frete, houve uma média de R$ 2,11 cobrados, sendo relativamente abaixo da média cobrada pelas demais compras. O motivo do cancelamento pode ser um erro no valor do frete.

O seller faz o envio de mercadorias dentro do prazo esperado, com exceção de algum problema ocorrido no dia 11/10. 



Great Imports
De 3197 pedidos, 239 foram suspensos ou cancelados. Parte dos pedidos foram cancelados ou suspendidos     durante o processo de envio, e outra parte foi suspendido quando houve a data de entrega da mercadoria.
A média entre a data de recebimento da mercadoria em setembro era de 8 dias, enquanto em outubro ela reduziu para 6 dias, sendo esse o motivo da melhora do indicar em Outubro.



<b>Plano de Ações que deverão ser tomados para maximização de resultados:</b>



Mari Eletro
Continuar honrando o prazo de entrega e os prazos de envio.
Para que a analise de dados e o plano de ação seja realmente efetivo , precisamos entender o motivo dos dados faltantes na planilha, se foi falta de preenchimento de campos necessários  ou erro na extração, pois 431 campos constam sem dados de entrega e envio (NULL), e grande parte não estão cancelados.
Coletar dados sobre a satisfação do cliente e detalhes do produto para entender o Real motivo de 6,5% dos pedidos do canal do mercado livre terem sidos cancelamentos.

Lojão Utilidades LTDA
Continuar honrando o prazo de entrega e tentar reduzir em 1 dia o prazo de envio, para que não fique abaixo do esperado.
Entender com o mercado livre o motivo dos cancelamento do dia 08/10, se foi indisponibilidade de estoque, ou erro no valor do frete incluso na plataforma e criar um plano de ação para que não aconteça mais inputs errados que prejudique as vendas futuras.
Entender com o Cliente o problema do envio fora do prazo de vários pedidos na data de 11/10, e montar um plano de ação para que não ocorra com frequência.
Houveram atrasos em entregas em diversos canais. Para que isso não aconteça, precisamos entender mais a fundo a localização, o tempo máximo de entrega de cada centro logístico, sua capacidade de venda em determinados estados e fazer negociação de prazo de entrega.

Great Imports
Entender com o cliente o motivo do cancelamento do pedido durante o processo do envio e após a entrega da mercadoria e entender o motivo dos cancelamentos dos pedidos já recebidos.
Para que o indicador de cancelamento seja reduzido, precisamos melhorar os dias médios da compra efetiva e do prazo do envio, assim teremos menos cancelamentos devido a interferência de datas, porém é uma decisão que deverá ser analisada com cautela com base em estoque e disponibilidade logística.
Verificar se conseguimos continuar reduzindo o prazo de médio de recebimento de mercadorias.



