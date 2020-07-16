Trabalho Final - R
================
Grupo 3 - Bruno Volpini, Dimitri Assis e Lucas Magesty
15/07/2020

# OBJETIVOS DO DESENVOLVIMENTO SUSTENTÁVEL: ANÁLISE DOS DADOS DO BANCO MUNDIAL

## Introdução

Os **Objetivos de Desenvolvimento Sustentável** são uma Agenda da
*Organização das Nações Unidas*, composta por 17 objetivos e 169 metas
interconectados a serem atingidos até 2030.

Nesta agenda estão previstas ações mundiais nas áreas de erradicação da
pobreza, segurança alimentar, agricultura, saúde, educação, igualdade de
gênero, redução das desigualdades, energia, água e saneamento, padrões
sustentáveis de produção e de consumo, mudança do clima, cidades
sustentáveis, proteção e uso sustentável dos oceanos e dos ecossistemas
terrestres, crescimento econômico inclusivo, infraestrutura,
industrialização, entre outros. [ACESSE O PORTAL DA ONU SOBRE OS
ODS](https://www.un.org/sustainabledevelopment/sustainable-development-goals/).

## Descrição da base de dados

A base de dados a ser analisada no relatório foi retirada do Data
Catalog do Banco Mundial ([ACESSE NESSE
LINK](https://datacatalog.worldbank.org/dataset/sustainable-development-goals)).
Na planilha, importada em .csv, há a descrição de 387 indicadores de 213
países, além de regiões do globo (como o Mundo Árabe e a África
Subsaariana), blocos econômicos (como a OCDE), divisões econômicas
(baixa e alta renda) e todos os continentes, à exceção da Antártida, no
período entre 1990 e 2019. Possui, ainda, mais de 3 milhões de células
(após leitura) e 32 MB de dados.

    ##  Country.Name       Country.Code       Indicator.Name     Indicator.Code    
    ##  Length:101781      Length:101781      Length:101781      Length:101781     
    ##  Class :character   Class :character   Class :character   Class :character  
    ##  Mode  :character   Mode  :character   Mode  :character   Mode  :character  
    ##                                                                             
    ##                                                                             
    ##                                                                             
    ##                                                                             
    ##      X1990                X1991                X1992           
    ##  Min.   :-3.620e+08   Min.   :-3.537e+08   Min.   :-2.138e+09  
    ##  1st Qu.: 4.000e+00   1st Qu.: 5.000e+00   1st Qu.: 5.000e+00  
    ##  Median : 3.800e+01   Median : 3.100e+01   Median : 3.200e+01  
    ##  Mean   : 6.877e+11   Mean   : 6.431e+11   Mean   : 6.469e+11  
    ##  3rd Qu.: 3.290e+03   3rd Qu.: 2.188e+03   3rd Qu.: 2.414e+03  
    ##  Max.   : 2.990e+15   Max.   : 3.357e+15   Max.   : 3.451e+15  
    ##  NA's   :78848        NA's   :75154        NA's   :74128       
    ##      X1993                X1994                X1995           
    ##  Min.   :-2.869e+08   Min.   :-1.142e+08   Min.   :-1.875e+09  
    ##  1st Qu.: 5.000e+00   1st Qu.: 5.000e+00   1st Qu.: 6.000e+00  
    ##  Median : 3.100e+01   Median : 3.200e+01   Median : 3.400e+01  
    ##  Mean   : 6.784e+11   Mean   : 7.202e+11   Mean   : 7.230e+11  
    ##  3rd Qu.: 2.268e+03   3rd Qu.: 2.518e+03   3rd Qu.: 2.249e+03  
    ##  Max.   : 3.495e+15   Max.   : 3.673e+15   Max.   : 3.974e+15  
    ##  NA's   :74267        NA's   :73898        NA's   :71675       
    ##      X1996                X1997                X1998           
    ##  Min.   :-1.127e+09   Min.   :-2.403e+08   Min.   :-2.408e+08  
    ##  1st Qu.: 6.000e+00   1st Qu.: 6.000e+00   1st Qu.: 6.000e+00  
    ##  Median : 3.200e+01   Median : 3.300e+01   Median : 3.100e+01  
    ##  Mean   : 7.889e+11   Mean   : 8.154e+11   Mean   : 8.191e+11  
    ##  3rd Qu.: 2.801e+03   3rd Qu.: 3.258e+03   3rd Qu.: 2.845e+03  
    ##  Max.   : 4.285e+15   Max.   : 4.487e+15   Max.   : 3.898e+15  
    ##  NA's   :72414        NA's   :72075        NA's   :71904       
    ##      X1999                X2000                X2001           
    ##  Min.   :-1.866e+09   Min.   :-4.550e+09   Min.   :-2.977e+09  
    ##  1st Qu.: 6.000e+00   1st Qu.: 6.000e+00   1st Qu.: 6.000e+00  
    ##  Median : 3.000e+01   Median : 2.800e+01   Median : 3.300e+01  
    ##  Mean   : 7.836e+11   Mean   : 6.418e+11   Mean   : 7.623e+11  
    ##  3rd Qu.: 1.654e+03   3rd Qu.: 1.000e+02   3rd Qu.: 3.710e+02  
    ##  Max.   : 3.928e+15   Max.   : 4.122e+15   Max.   : 4.272e+15  
    ##  NA's   :69424        NA's   :59399        NA's   :64400       
    ##      X2002                X2003                X2004           
    ##  Min.   :-1.017e+09   Min.   :-3.364e+09   Min.   :-2.041e+10  
    ##  1st Qu.: 6.000e+00   1st Qu.: 6.000e+00   1st Qu.: 6.000e+00  
    ##  Median : 3.300e+01   Median : 3.300e+01   Median : 3.400e+01  
    ##  Mean   : 7.921e+11   Mean   : 8.668e+11   Mean   : 8.907e+11  
    ##  3rd Qu.: 4.300e+02   3rd Qu.: 4.000e+02   3rd Qu.: 1.970e+02  
    ##  Max.   : 4.464e+15   Max.   : 4.763e+15   Max.   : 4.964e+15  
    ##  NA's   :63312        NA's   :64099        NA's   :62327       
    ##      X2005                X2006                X2007           
    ##  Min.   :-2.509e+10   Min.   :-2.397e+09   Min.   :-2.968e+10  
    ##  1st Qu.: 6.000e+00   1st Qu.: 6.000e+00   1st Qu.: 6.000e+00  
    ##  Median : 2.900e+01   Median : 3.300e+01   Median : 3.500e+01  
    ##  Mean   : 8.439e+11   Mean   : 9.734e+11   Mean   : 1.051e+12  
    ##  3rd Qu.: 1.000e+02   3rd Qu.: 1.000e+02   3rd Qu.: 1.080e+02  
    ##  Max.   : 5.193e+15   Max.   : 5.478e+15   Max.   : 5.832e+15  
    ##  NA's   :57471        NA's   :60196        NA's   :59332       
    ##      X2008                X2009                X2010           
    ##  Min.   :-9.502e+09   Min.   :-8.826e+09   Min.   :-2.201e+10  
    ##  1st Qu.: 6.000e+00   1st Qu.: 6.000e+00   1st Qu.: 6.000e+00  
    ##  Median : 3.400e+01   Median : 3.300e+01   Median : 2.700e+01  
    ##  Mean   : 1.160e+12   Mean   : 1.174e+12   Mean   : 1.273e+12  
    ##  3rd Qu.: 1.000e+02   3rd Qu.: 1.000e+02   3rd Qu.: 9.900e+01  
    ##  Max.   : 6.176e+15   Max.   : 6.462e+15   Max.   : 6.864e+15  
    ##  NA's   :59760        NA's   :58889        NA's   :53008       
    ##      X2011                X2012                X2013           
    ##  Min.   :-6.008e+09   Min.   :-1.635e+10   Min.   :-2.964e+10  
    ##  1st Qu.: 6.000e+00   1st Qu.: 6.000e+00   1st Qu.: 6.000e+00  
    ##  Median : 3.400e+01   Median : 3.300e+01   Median : 3.300e+01  
    ##  Mean   : 1.442e+12   Mean   : 1.538e+12   Mean   : 1.706e+12  
    ##  3rd Qu.: 1.000e+02   3rd Qu.: 1.000e+02   3rd Qu.: 1.000e+02  
    ##  Max.   : 7.832e+15   Max.   : 8.616e+15   Max.   : 9.934e+15  
    ##  NA's   :54880        NA's   :55649        NA's   :56711       
    ##      X2014                X2015                X2016           
    ##  Min.   :-1.521e+10   Min.   :-1.951e+10   Min.   :-2.894e+10  
    ##  1st Qu.: 6.000e+00   1st Qu.: 6.000e+00   1st Qu.: 5.000e+00  
    ##  Median : 3.600e+01   Median : 2.900e+01   Median : 2.800e+01  
    ##  Mean   : 1.713e+12   Mean   : 1.776e+12   Mean   : 1.885e+12  
    ##  3rd Qu.: 1.000e+02   3rd Qu.: 9.900e+01   3rd Qu.: 9.900e+01  
    ##  Max.   : 1.152e+16   Max.   : 1.153e+16   Max.   : 1.315e+16  
    ##  NA's   :53681        NA's   :53751        NA's   :52940       
    ##      X2017                X2018                X2019               X          
    ##  Min.   :-3.614e+10   Min.   :-2.393e+11   Min.   :-7.927e+10   Mode:logical  
    ##  1st Qu.: 6.000e+00   1st Qu.: 7.000e+00   1st Qu.: 9.000e+00   NA's:101781   
    ##  Median : 3.900e+01   Median : 4.000e+01   Median : 5.000e+01                 
    ##  Mean   : 2.332e+12   Mean   : 2.241e+12   Mean   : 4.696e+12                 
    ##  3rd Qu.: 1.000e+02   3rd Qu.: 4.980e+02   3rd Qu.: 1.620e+04                 
    ##  Max.   : 1.532e+16   Max.   : 1.484e+16   Max.   : 1.583e+16                 
    ##  NA's   :59439        NA's   :68985        NA's   :86339

### Perguntas Exploratórias

Isso posto, o foco do grupo neste trabalho é analisar, dentre os mais de
387 indicadores disponíveis para os Objetivos de Desenvolvimento
Sustentável, 22 indicadores em **três eixos**: **educação, economia e
sustentabilidade**, em um comparativo Brasil, América Latina e Mundo.

  - **Educação (ODS 4)**: o Brasil, comparado com LatAm e Mundo,
    desenvolveu sua educação nos últimos 30 anos? Se sim, sob quais
    aspectos?

  - **Economia (ODSs 1, 2, 8, 9 e 10)**: Qual a situação econômica do
    Brasil, comparado com LatAm e Mundo, na perspectiva do crescimento e
    desigualdade?

  - **Sustentabilidade (ODSs 13 e 15)**: O Brasil, comparado com LatAm e
    Mundo, é sustentável e preserva seus recursos?

## Análise Exploratória

## Considerações finais
