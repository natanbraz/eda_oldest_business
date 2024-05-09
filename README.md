# Quais são os negócios mais antigos do mundo? 🏢

A fim de responder essa pergunta, o site BusinessFinancing.co.uk realizou uma pesquisa sobre os negócios mais antigos do mundo. O resultado dessa pesquisa esta foi resumido no dataset <code>businesses</code> dentro da pasta <code>dataset</code>. Além desse dataset, estão disponiveis outros dois dataset auxiliares: <code>categories</code> e <code>countries</code>.

A partir desses datasets, realizei uma analise exploratória bastante simples, através da biblioteca <code>pandas</code>, para verificar algumas caracteristicas básicas sobre os dados. Os resultados encontrados a partir dessa analise estão resumidas nesse texto e o código pode ser encontrado dentro do notebook "<code>eda_notebook</code>". 

O **objetivo** desta exploração e analise é colocar em prática alguns conceitos básicos de <code>pandas</code>, de escrita em <code>markdown</code>, utilização do <code>github</code> para armazenamento dessa analise e, não menos importante, a explicação dos resultados encontrados. 

Outro destaque, é que essa analise exploratória foi feita durante o curso de *Associate Data Scientist in Python* da escola **[datacamp](https://www.datacamp.com/)**.

## Descrição dos datasets

Os datasets utilizados estão localizados na pasta <code>datasets</code> e são divididos da seguinte maneira:
<h3 id="countries"><code>business</code></h3>
<table>
<thead>
<tr>
<th style="text-align:left;">coluna</th>
<th>tipo</th>
<th>descricao</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;"><code>business</code></td>
<td>string</td>
<td>Nome do negócio.</td>
</tr>
<tr>
<td style="text-align:left;"><code>year_founded</code></td>
<td>int</td>
<td>Ano de fundação.</td>
</tr>
<tr>
<td style="text-align:left;"><code>category_code</code></td>
<td>string</td>
<td>Codigo para a categoria do negócio.</td>
</tr>
<tr>
<td style="text-align:left;"><code>country_code</code></td>
<td>string</td>
<td>Código do Pais (formato ISO 3166-1 3-letter).</td>
</tr>
</tbody>
</table>
<h3 id="countries"><code>countries</code></h3>
<table>
<thead>
<tr>
<th style="text-align:left;">coluna</th>
<th>tipo</th>
<th>descricao</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;"><code>country_code</code></td>
<td>string</td>
<td>Código do País (formato ISO 3166-1 3-letter).</td>
</tr>
<tr>
<td style="text-align:left;"><code>country</code></td>
<td>string</td>
<td>Nome do País.</td>
</tr>
<tr>
<td style="text-align:left;"><code>continent</code></td>
<td>string</td>
<td>Nome do continente aonde o país está.</td>
</tr>
</tbody>
</table>
<h3 id="categories"><code>categories</code></h3>
<table>
<thead>
<tr>
<th style="text-align:left;">coluna</th>
<th>tipo</th>
<th>descricao</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;"><code>category_code</code></td>
<td>string</td>
<td>Código para a categoria do negócio.</td>
</tr>
<tr>
<td style="text-align:left;"><code>category</code></td>
<td>string</td>
<td>Descrição da categoria do negócio.</td>
</tr>
</tbody>
</table>


## Resultados encontrados 

Após realizar a analise exploratória dos dados, encontramos alguns dados interessantes sobre os negócios mais antigos do mundo:

1. O negócio mais antigo do mundo é **Kongō Gumi** fica localizado no Japão e o registro mostra que foi fundado em 578. O setor desse negócio era a "Construção". Além desse, os 10 negócios mais antigos do mundo, segundo o nosso dataset, são:

| business                           | year_founded | country        | category                          |
|------------------------------------|--------------|----------------|-----------------------------------|
| Kongō Gumi                         | 578          | Japan          | Construction                      |
| St. Peter Stifts Kulinarium        | 803          | Austria        | Cafés, Restaurants & Bars         |
| Staffelter Hof Winery              | 862          | Germany        | Distillers, Vintners, & Breweries |
| Monnaie de Paris                   | 864          | France         | Manufacturing & Production        |
| The Royal Mint                     | 886          | United Kingdom | Manufacturing & Production        |
| Sean's Bar                         | 900          | Ireland        | Cafés, Restaurants & Bars         |
| Marinelli Bell Foundry             | 1040         | Italy          | Manufacturing & Production        |
| Affligem Brewery                   | 1074         | Belgium        | Distillers, Vintners, & Breweries |
| Munke Mølle                        | 1135         | Denmark        | Manufacturing & Production        |
| Ma Yu Ching's Bucket Chicken House | 1153         | China          | Cafés, Restaurants & Bars         |


2. O negócio mais antigo da América do Sul é a **Casa Nacional de Moneda** localizada no Peru e fundada no ano de 1565. Esse "empreendimento" é do ano do setor de Banking & Finance. Além desse, os outros 10 empreendimentos mais antigos da América do Sul são: 

| business                             | year_founded | country                           | category                   |
|--------------------------------------|--------------|-----------------------------------|----------------------------|
| Casa Nacional de Moneda              | 1565         | Peru                              | Banking & Finance          |
| Casa de Moneda de Colombia           | 1621         | Colombia                          | Manufacturing & Production |
| Hacienda Chuao                       | 1660         | Venezuela, Bolivarian Republic of | Food & Beverages           |
| Casa da Moeda do Brasil              | 1694         | Brazil                            | Manufacturing & Production |
| Famae                                | 1811         | Chile                             | Defense                    |
| Bank of the Province of Buenos Aires | 1822         | Argentina                         | Banking & Finance          |
| Banks DIH                            | 1840         | Guyana                            | Food & Beverages           |
| Banco Nacional de Bolivia            | 1871         | Bolivia, Plurinational State of   | Banking & Finance          |
| Cafe Brasilero                       | 1877         | Uruguay                           | Cafés, Restaurants & Bars  |

3. Olhando para cada continente, também podemos localizar e encontrar os registros de empreendimentos mais antigos por continente. O resultado mostra que Asia e Europe tem os empreendimentos mais antigos. Enquanto a Oceania tem o empreendimento "mais recente" entre eles: 

| business                    | year_founded | continent     | country   | category                   |
|-----------------------------|--------------|---------------|-----------|----------------------------|
| Mauritius Post              | 1772         | Africa        | Mauritius | Postal Service             |
| Kongō Gumi                  | 578          | Asia          | Japan     | Construction               |
| St. Peter Stifts Kulinarium | 803          | Europe        | Austria   | Cafés, Restaurants & Bars  |
| La Casa de Moneda de México | 1534         | North America | Mexico    | Manufacturing & Production |
| Australia Post              | 1809         | Oceania       | Australia | Postal Service             |
| Casa Nacional de Moneda     | 1565         | South America | Peru      | Banking & Finance          |

4. Olhando a quantidade de negócios do nosso DataFrame, podemos também olhar para a quantidade de negócios em cada categoria. O resultado mostrou que as 5 categorias com mais negócios no nosso dataset são: 

| category                          | business_count |
|-----------------------------------|----------------|
| Banking & Finance                 | 37             |
| Distillers, Vintners, & Breweries | 22             |
| Aviation & Transport              | 19             |
| Postal Service                    | 16             |
| Manufacturing & Production        | 15             |


5. Além disso, olhamos qual foi o ano de fundação mais antigo para cada categoria e país. O resultado, encontra-se abaixo. Os destaques ficam para a categoria de "Manufacturing & Production", tendo sido os negócios mais antigos na média entre os continentes,  e "Banking & Finance" que aparece em todos os continentes.

| continent     | category                          | year_founded |
|---------------|-----------------------------------|--------------|
| Africa        | Agriculture                       | 1947         |
| Africa        | Aviation & Transport              | 1854         |
| Africa        | Banking & Finance                 | 1892         |
| Africa        | Distillers, Vintners, & Breweries | 1933         |
| Africa        | Energy                            | 1968         |
| Africa        | Food & Beverages                  | 1878         |
| Africa        | Manufacturing & Production        | 1820         |
| Africa        | Media                             | 1943         |
| Africa        | Mining                            | 1962         |
| Africa        | Postal Service                    | 1772         |
| Asia          | Agriculture                       | 1930         |
| Asia          | Aviation & Transport              | 1858         |
| Asia          | Banking & Finance                 | 1830         |
| Asia          | Cafés, Restaurants & Bars         | 1153         |
| Asia          | Conglomerate                      | 1841         |
| Asia          | Construction                      | 578          |
| Asia          | Defense                           | 1808         |
| Asia          | Distillers, Vintners, & Breweries | 1853         |
| Asia          | Energy                            | 1928         |
| Asia          | Food & Beverages                  | 1820         |
| Asia          | Manufacturing & Production        | 1736         |
| Asia          | Media                             | 1931         |
| Asia          | Mining                            | 1913         |
| Asia          | Postal Service                    | 1800         |
| Asia          | Retail                            | 1883         |
| Asia          | Telecommunications                | 1885         |
| Asia          | Tourism & Hotels                  | 1584         |
| Europe        | Agriculture                       | 1218         |
| Europe        | Banking & Finance                 | 1606         |
| Europe        | Cafés, Restaurants & Bars         | 803          |
| Europe        | Consumer Goods                    | 1649         |
| Europe        | Defense                           | 1878         |
| Europe        | Distillers, Vintners, & Breweries | 862          |
| Europe        | Manufacturing & Production        | 864          |
| Europe        | Media                             | 1999         |
| Europe        | Medical                           | 1422         |
| Europe        | Mining                            | 1248         |
| Europe        | Postal Service                    | 1520         |
| Europe        | Telecommunications                | 1912         |
| Europe        | Tourism & Hotels                  | 1230         |
| North America | Agriculture                       | 1638         |
| North America | Aviation & Transport              | 1870         |
| North America | Banking & Finance                 | 1891         |
| North America | Distillers, Vintners, & Breweries | 1703         |
| North America | Food & Beverages                  | 1920         |
| North America | Manufacturing & Production        | 1534         |
| North America | Media                             | 1909         |
| North America | Retail                            | 1670         |
| North America | Tourism & Hotels                  | 1770         |
| Oceania       | Banking & Finance                 | 1861         |
| Oceania       | Postal Service                    | 1809         |
| South America | Banking & Finance                 | 1565         |
| South America | Cafés, Restaurants & Bars         | 1877         |
| South America | Defense                           | 1811         |
| South America | Food & Beverages                  | 1660         |
| South America | Manufacturing & Production        | 1621         |


# Conclusão

A partir da realização dessa EDA (Analise exploratória de Dados) bastante simples, observamos algumas caracteristicas importantes sobre os negócios. A primeira é que boa parte dos negócios mais antigos do nosso dataset são da categoria "Banking & Finance". Além disso, essa categoria foi a única que esteve presente em praticamente todos os continentes. E a segunda, é que a Europa é o país com mais negócios antigos em nosso dataset. Observamos isso, pela lista dos 10 negócios mais antigos do mundo, em que 8 estão dentro da Europa.
