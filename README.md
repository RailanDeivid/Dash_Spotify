# Dashboard Spotify

<p align="center">
  <img src="https://uploads.jovemnerd.com.br/wp-content/uploads/2021/08/spotify-plano-mais-barato.jpg">
</p>

## Dashboard:
Os dados que analisados foram tirados do meu Spotify, dados esses de tudo que foi reproduzido no período de 01/2021 até 08/2021.
##### Que pode se acessado pelo link abaixo:
**[Dashboard Spotify Analise](https://app.powerbi.com/view?r=eyJrIjoiMTg1ZWIwNDEtNGRiNy00NTEzLWE0ZTEtZWQ0YjY4YmJlYTg3IiwidCI6ImI0MjE1NzJlLWM1NTMtNDJlZC04ZjgyLWYwZDMzNTViMTk3YyJ9)**

## Elementos do Dash
O dashboard foi estruturado em apenas um relatório conténdo tudos que foi escutado no período. Sendo eles, musicas mais tocadas, podcasts mais tocados, quantidade total de musicas, 
total de artistas e horas tocadas durante o tempo.

#### Os dados acerca de cada elemento contido na página estará disposto da seguinte maneira abaixo:

### Geral
[![Dash-Spotify-image.jpg](https://i.postimg.cc/MHyH8WzF/Dash-Spotify-image.jpg)](https://postimg.cc/H8kdw1cw)

Essa é a visão geral da página. Nela é possível observar o seguintes elementos:

#### Painel Geral
[![Captura-de-tela-2021-10-01-100830.jpg](https://i.postimg.cc/xd1PT1ph/Captura-de-tela-2021-10-01-100830.jpg)](https://postimg.cc/xXBm6n23)

Nesse painel principal mostra o total de horas escutadas, a quantidade de horas escutadas e o total de artistas tocados.

## Horas por dia da Semana
[![Captura-de-tela-2021-10-01-100907.jpg](https://i.postimg.cc/0j4Nmc97/Captura-de-tela-2021-10-01-100907.jpg)](https://postimg.cc/m1QRW3zr)

Nessa visualização foi usado um gráfico de barras clusterizado (barras horizontais). 
Nele mostra a quantidade de horas escutadas em cada dia da semana.

## As mais Tocadas
[![Captura-de-tela-2021-10-01-100927.jpg](https://i.postimg.cc/MKb954C6/Captura-de-tela-2021-10-01-100927.jpg)](https://postimg.cc/svxPDnfq)

Aqui temos uma visão das musicas que foram tocadas mais vezes no período de 01/2021 até 08/2021.

## Horas Escutadas por período
[![Captura-de-tela-2021-10-01-100945.jpg](https://i.postimg.cc/nhdr4FTv/Captura-de-tela-2021-10-01-100945.jpg)](https://postimg.cc/YvWtkw59)

Esse gráfico já trás uma vizualização mais geral do total de horas escutadas em cadas mês.

## Bandas mais tocadas
[![Captura-de-tela-2021-10-01-101009.jpg](https://i.postimg.cc/6QCGKJtg/Captura-de-tela-2021-10-01-101009.jpg)](https://postimg.cc/Nyf08nyk)

Aqui podemos ver quais foram as bandas mais escutadas.

## OS Podcasts mais Escutados
[![Captura-de-tela-2021-10-01-101025.jpg](https://i.postimg.cc/wxLhhGPw/Captura-de-tela-2021-10-01-101025.jpg)](https://postimg.cc/t7RZb296)

E por fim temos a nossa ultima vizualização que trás os podcasts mais escutados.

## ETL
O processo de ETL foi feito através do Python, a partir dos 4 arquivos json nomeados de (StreamingHistory0, StreamingHistory1, StreamingHistory2) onde contém os dados de tudos que foi tocado
no meu Spotify e o arquivo (YourLibrary) que contém os nomes dos artista e podcasts que sigo e escuto. Todos os dados foram fornecidos pelo Spotify.

**[Notebook e Códigos](https://github.com/RailanDeivid/Dash_Spotify/blob/main/Tratando_dados.ipynb)**

### Dados:
Cada linha da base de dados corresponde a uma musica ou um podcast tocado, cada coluna contém um atributo, sendo eles:

- "endTime" 
Data e hora de quando o musica/podcast foi tocado no formato UTC (fuso horário universal coordenado).
- "artistName" 
Nome do "criador" de cada fluxo (por exemplo, o nome do artista, se for uma faixa de música ou nome do podcast).
- "trackName" 
Nome dos itens ouvidos ou assistidos (por exemplo, título da faixa musical ou nome do vídeo).
- "msPlayed" 
Significa quantos milissegundos a faixa foi ouvida.


#### O tratamento de dados consistiu em:

  * Foi feito a concatenação dos 4 arquivos fornecidos pelo Spotify
  * Foram criadas novas colunas com as transformações de milesegundos em minutos e em seguida a trasnformação de minutos em horas
  * Trasnformação da coluna contendo datas em Datetime
  * Foi feito a remoção de algumas colunas que não será necessária para a analise 
  * Foi feito um filtro na coluna data apenas coms as datas do ano de 2021
  * Foi criado uma nova coluna de data com a formatação brasileira
  * Foi feito um filtro geral nos dados usando o arquivo (YourLibrary) que contém os nomes dos artista e podcasts que sigo e escuto, apenas para mostras os dados que foram escutados apenas por mim
  * Por fim, todas as alterações feitas acima foram trasnsformada em um novo aquivo csv.
  
* Analises

  * Foi criando 3 tabelas para uam melhor analise:
      * As bandas mais escutadas
      * Podcasts mais tocados
      * Musicas tocadas mais vezes
      
      


## Conclusão

Essa foi um bréve analise do que escutei no período de 01/2021 até 08/2021.

Há pouco tempo atrás fiz uma analisei com os dados do meu Spotify usando o python com algumas visualizações básicas das bibliotecas Matplotlib e Seaborn e disponibilizei os dados no 
meu GitHub e os insights no meu blog do Medium.

### Medium:
**[Analisando os dados do meu Spotify — Python.](https://railandeivid.medium.com/analisando-os-dados-do-meu-spotify-python-5ba60481761d)**

### Código:
**[Notebook](https://github.com/RailanDeivid/Analise_dados_meu_spotify.git)**



