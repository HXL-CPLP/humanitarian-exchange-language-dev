# Humanitarian Exchange Language Dev

> Lista de serviços gratuitos e ferramentas para pessoas desenvolvedoras que implemente o Padrão HXL ("The Humanitarian Exchange Language").

[![GitHub stars](https://img.shields.io/github/stars/HXL-CPLP/humanitarian-exchange-language-dev?style=social)](https://github.com/HXL-CPLP/humanitarian-exchange-language-dev)

[![Grupo de Usuários do Padrão HXL da Comunidade dos Países de Língua Portuguesa](https://hxl.etica.ai/img/banner-hxl-cplp.png)](https://padrao-hxl.etica.ai/)
<hr>

## HDX Tools

[![Screenshot of HDX Tools](http://blog.dev.hxlstandard.org/wp-content/uploads/HDXTools.png)](https://tools.humdata.org/)

[HDX Tools](https://tools.humdata.org/)  oferecem ferramentas interativas para trabalhar online em dados com #HXL.

### [Quick Charts](https://tools.humdata.org/quickcharts/)

Crie e compartilhe gráficos e tabelas interativas com seus dados.

### [Tag Assist](https://tools.humdata.org/examples/hxl/)

Ajuda para encontrar as hashtags HXL certas para seus dados.

### [Data Check](https://tools.humdata.org/wizard/#datacheck)

Carregue seus dados e receba um relatório de volta destacando possíveis erros.

## [HXL Proxy](https://proxy.hxlstandard.org/)

[![](http://blog.dev.hxlstandard.org/wp-content/uploads/HXLProxy_screenshot.png)](https://proxy.hxlstandard.org/)

Uma ferramenta on-line gratuita para limpar, transformar, mesclar e validar dados marcados com HXL. O HXL Proxy permite executar muitas operações que normalmente exigiriam um banco de dados, mesmo quando os conjuntos de dados são distribuídos pelos serviços da Web e na nuvem.

Algumas das operações possíveis incluem:

- Anexar conjuntos de dados
- Anexar conjuntos de dados por lista externa
- Limpeza de dados
- Contar linhas
- Cortar colunas
- Linhas com redução de redundância
- Explode data
- Preencher células vazias
- Extração de valor JSONPath
- Mesclar de outro conjunto de dados
- Renomear coluna
- Substituir dados
- Substituir dados num mapa externo
- Selecionar linhas
- Classificar linhas

O HXL Proxy foi projetado para alto desempenho, funciona anonimamente e foi testado com conjuntos de dados de origem de até 500.000 linhas.

Você cria uma receita que contém uma série de etapas para transformar os dados. Você pode salvar o resultado da sua transformação como uma receita ao vivo que permitirá que os usuários baixem versões CSV ou JSON de seus dados modificados, que serão atualizados automaticamente quando a origem for alterada.

## [Biblioteca HXL no Python e ferramentas de linha de comando](https://github.com/HXLStandard/libhxl-python)

Biblioteca Python e ferramentas de linha de comando para validar, limpar e transformar dados marcados com HXL em um ambiente em lote, otimizados para uso com grandes conjuntos de dados. Por exemplo, o comando a seguir produzirá um relatório do número de organizações diferentes mencionadas em um conjunto de dados:

```hxlcount -t org mydata.csv```

## [Biblioteca  HXL do navegador Javascript](https://github.com/HXLStandard/libhxl-js)

Biblioteca Javascript no estilo JQuery para processar dados HXL dentro do navegador da Web, sem a necessidade de suporte de um servidor (especialmente valioso para aplicativos da Web interativos). Por exemplo, esta linha de código carregará um conjunto de dados de 3W e produzirá um relatório do número de atividades em cada região:

```hxl.load('http://example.org/3w.csv', function (dataset) {
var region_stats = dataset.count('adm1');
// do something with the stats
});
```

## [HXL em R](https://dirkschumacher.github.io/rhxl/)

Módulo HXL para o [R](https://en.wikipedia.org/wiki/R_(programming_language)), escrito e mantido por [Dirk Schumacher](https://github.com/dirkschumacher). Exemplo:

```data_url <- "http://ourairports.com/countries/VN/airports.hxl"
hxl_data <- as_hxl(read.csv(data_url))
head(hxl_data)
#> # A tibble: 6 × 20
#>      id ident           type                               name
#>   <int> <chr>          <chr>                              <chr>
#> 1 26708  VVTS  large_airport Tan Son Nhat International Airport
#> 2 26700  VVNB  large_airport      Noi Bai International Airport
#> 3 26697  VVDN  large_airport      Da Nang International Airport
#> 4 26693  VVCR medium_airport                   Cam Ranh Airport
#> 5 26705  VVPQ medium_airport     Phu Quoc International Airport
#> 6 26702  VVPB medium_airport                    Phu Bai Airport
#> # ... with 16 more variables: latitude_deg <dbl>, longitude_deg <dbl>,
#> #   elevation_ft <int>, continent <chr>, iso_country <chr>,
#> #   iso_region <chr>, municipality <chr>, scheduled_service <int>,
#> #   gps_code <chr>, iata_code <chr>, local_code <chr>, home_link <chr>,
#> #   wikipedia_link <chr>, keywords <chr>, score <int>, last_updated <dttm>
```

## [Proxy HXL](https://proxy.hxlstandard.org/)

[![Screenshot of the HXL Proxy](http://blog.dev.hxlstandard.org/wp-content/uploads/HXLProxy_screenshot.png)](https://proxy.hxlstandard.org/)

## [csvhuman para Ruby](https://github.com/csvreader/csvhuman)

A Ruby GEM for reading HXL-hashtagged CSV data. Written by Gerald Bauer.

<hr>
Mais detalhes estão disponíveis em https://github.com/HXLStandard/hxl-proxy/wiki/Use-cases

A documentação completa do usuário está disponível em [HXL Proxy wiki](https://github.com/HXLStandard/hxl-proxy/wiki).

