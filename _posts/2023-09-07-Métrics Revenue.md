---
date: 2023-09-07
title: Métrics Revenue
categories:

featured_image: "https://raw.githubusercontent.com/Giovanacarmazio/portifolio/main/images/M%C3%A9trics%20Revenue%201.jpg"
recipe:
 
---



 Métrics Revenue



![](https://raw.githubusercontent.com/Giovanacarmazio/portifolio/main/images/M%C3%A9trics%20Revenue%201.jpg)
![](https://raw.githubusercontent.com/Giovanacarmazio/portifolio/main/images/M%C3%A9trics%20Revenue%202.jpg)
![](https://raw.githubusercontent.com/Giovanacarmazio/portifolio/main/images/M%C3%A9trics%20Revenue%203.jpg)


Métrics Revenue - Power BI e DAX.

Esse dashboard fornece uma visão geral o desempenho financeiro do conjunto de dados estudado.
Também nos permite identificar oportunidades de crescimento, otimizar nossas estratégias de vendas e tomar decisões mais embasadas. 
O Objetivo principal foi a criação de novos cartões disponibilizados pela Microsoft, testando a inclusão de graficos dinamicos nos cartões.

A Medida dax Utilizada foi:

Sparkline =
VAR Defs = "<defs>
    <linearGradient id='grad' x1='0' y1='25' x2='0' y2='50' gradientUnits='userSpaceOnUse'>
        <stop stop-color='navy' offset='0' />
        <stop stop-color='transparent' offset='1' />
    </linearGradient>
</defs>"
VAR XMinDate = MIN(dCalendario[Data])
VAR XMaxDate = MAX(dCalendario[Data])
VAR YMinValue = MINX(VALUES(dCalendario[Data]), CALCULATE([Revenue]))
VAR YMaxValue = MAXX(VALUES(dCalendario[Data]), CALCULATE([Revenue]))
VAR SparklineTable = ADDCOLUMNS(
    SUMMARIZE('adidas_sales', dCalendario[Data]),
        "X", INT(150 * DIVIDE(dCalendario[Data] - XMinDate, XMaxDate - XMinDate)),
        "Y", INT(50 * DIVIDE([Revenue] - YMinValue, YMaxValue - YMinValue))
)
VAR Lines = CONCATENATEX(SparklineTable, [X] & "," & 50 - [Y], " ", dCalendario[Data])
VAR SVGImageURL = IF(HASONEVALUE(dCalendario[Data]),
    "data:image/svg+xml;utf8," & 
    "<svg xmlns='http://www.w3.org/2000/svg' x='0px' y='0px' viewBox='0 0 150 50'>" & Defs &
    "<polyline fill='url(#grad)' fill-opacity='0.3' stroke='navy' 
      stroke-width='3' points=' 0 50 " & Lines & 
      " 150 150 Z '/></svg>",
    BLANK()
)
RETURN SVGImageURL

Após a criação da Medida, é só clicar no seu card, ir em Formato/ Cartões / Imagem e em URL de Imagem, selecionar a medida dax criada.


<a href="https://app.powerbi.com/view?r=eyJrIjoiMTdjZjE4OTYtNTUxNy00Y2EyLTk4ZjItYzhlNTE2MjUyOGQxIiwidCI6ImU5YzYxMzhlLTQyZmUtNGM3MS1iMWFkLTc1ZjA1NTdiOWI0NSJ9">Clique aqui</a> e confira o Dashboard publicado.
Nesse Link, você pode fazer filtros e verificar interações de painés.

