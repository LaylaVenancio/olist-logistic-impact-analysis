# olist-logistic-impact-analysis

## 1. Contexto

O foco do projeto é realizar a análise do **impacto da eficiência logística na satisfação do cliente em marketplaces do Brasil**, com base no [conjunto de dados disponibilizado pela Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), que compreende um universo de aproximadamente 100 mil pedidos, realizados entre os anos de 2016 e 2018.

O dataset foi estruturada em tabelas (.csv) e a ferramenta escolhida para lidar com elas foi o **Google Colab**, utilizando as bibliotecas **Pandas, Numpy, Seaborn** e **Matplotlib** da linguagem  **Python**. 

## 2. Principais Insights

1. **A eficiência logística é determinante na avaliação do cliente**. Considerando uma escala de 1 a 5, enquanto pedidos antecipados ou no prazo mantêm uma mediana de avaliação 5.0, pedidos atrasados sofrem uma queda drástica na percepção de valor, com mediana 1.0. Além disso, 62% dos pedidos em atraso que receberam uma avaliação, foi de 1 ou 2.
2. **O risco de atraso é diretamente proporcional à distância geográfica**. Pedidos que percorrem mais de 2.000 km apresentam uma taxa de atraso de 12,1%, o que representa mais que o dobro do índice registrado em trajetos curtos (até 500 km), que é de 5,6%.
3.**Identificou-se um pico de atrasos entre novembro de 2017 e março de 2018**, com destaque para o mês de março (18,9%). Esse comportamento está atrelado ao aumento de demanda em **datas de alto consumo**, como Black Friday, Natal e Dia do Consumidor, além dos reflexos operacionais do feriado de Carnaval.
4. Existe uma correlação positiva (embora fraca, de 0,27) entre o **cumprimento do prazo de postagem por parte do vendedor** e a entrega do pedido ao cliente final dentro do prazo estipulado.
5. **Existe um desafio logístico mais acentuado nas regiões Nordeste (12,7% de atraso) e Norte (8,6% de atraso)**, sendo as únicas que superam a média geral de 6,8%. Em contrapartida, as regiões Sul e Sudeste, apesar do volume massivo de pedidos, mantêm os menores índices de atraso.
6. **As regiões Sudeste (4.030) e Nordeste (1.141) concentram o maior volume absoluto de clientes afetados por atrasos**, sendo assim, torna-se indispensável priorizá-las em futuras intervenções de melhoria logística.

## 3. Método 

1. Tratamento e Limpeza: Identificação e correção de nulos, duplicatas e tipos incorretos
2. Consolidação: Realização de Joins entre as tabelas originais para a criação de um dataset unificado com a granularidade de pedidos entregues.  
3. Enriquecimento de Dados: Criação de métricas logísticas essenciais, como o cálculo da distância entre vendedor e comprador (km) e o status de pontualidade da postagem e da entrega.  
4. Análise e Visualização: Aplicação de correlação de Pearson e estatística descritiva, culminando na criação de gráficos exploratórios e um [Dashboard no Power BI](https://app.powerbi.com/view?r=eyJrIjoiMmZmOTM1MmYtYjE2OS00OTAxLTk5ZDUtOTkyOGMzOTBmMTMyIiwidCI6IjhlZWNhNDA0LWE0N2QtNDU1NS1hMmQ0LTBmMzYxOTA0MWM5YyJ9) para suporte à decisão executiva.
