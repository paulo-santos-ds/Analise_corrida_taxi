# Análise Corridas de Taxi

## Descrição do Projeto
Este projeto tem como objetivo analisar os dados de um aplicativo fictício de caronas. Encontrar padrões nas informações disponíveis, entender as preferências dos passageiros e o impacto de fatores externos nas corridas. 
 
 ** Ferramentas e Bibliotecas Utilizadas **
* Python: Linguagem principal utilizada para a análise.
* Pandas: Biblioteca para manipulação e análise de dados.
* Numpy e scipy: Biblioteca que visa possibilitar a computação numérica com Python
* Matplotlib.pyplot e seaborn: Bibliotecas para criação de gráficos.
Tabelas

Para este projeto foram construídas tabelas através de consultas a banco de dados utilizando SQL.
**Descrição Banco de Dados** Um banco de dados com informações sobre corridas de táxi em Chicago:
* tabela neighborhoods: dados sobre os bairros da cidade
   * nome: nome do bairro
   * neighborhood_id: código do bairro
* tabela cabs: dados sobre os táxis
   * cab_id: código do veículo
   * vehicle_id: a identificação técnica do veículo
   * company_name: a empresa proprietária do veículo
* tabela trips: dados sobre corridas
   * trip_id: código da corrida
   * cab_id: código do veículo que opera a corrida
   * start_ts: data e hora do início da corrida (tempo arredondado para a hora)
   * end_ts: data e hora do fim da corrida (tempo arredondado para a hora)
   * duration_seconds: duração da corrida em segundos
   * distance_miles: distância do percurso em milhas
   * pickup_location_id: código do bairro de retirada
   * dropoff_location_id: código do bairro de entrega
* tabela weather_records: dados sobre o clima
   * record_id: código de registro meteorológico
   * ts: gravar data e hora (tempo arredondado para a hora)
   * temperatura: temperatura quando o registro foi feito
   * descrição: breve descrição das condições meteorológicas, ex. "chuva leve" ou "nuvens esparsas"
**Esquema de tabela**
**Tabelas Utilizadas**
* moved_project_sql_result_01: número de corridas para cada empresa de táxi
* moved_project_sql_result_04: número médio de viagens que terminaram em cada bairro
* moved_project_sql_result_07: dados sobre viagens do Loop para o Aeroporto Internacional O'Hare.
Metodologia
**Extração Dados Banco**
* Querys d SQl para realizar a extração dos dados necessários para análise
**Análise Exploratória de Dados**
* Importar as bibliotecas necessárias
* Carregar e visualizar os dados
**Análise dos Dados**
* Quantidade de viagens por companhia
* Quantidade de viagens médias por bairro
**Criando e Validando Hipóteses**
* A duração média dos passeios do Loop para o Aeroporto Internacional O'Hare muda nos sábados chuvosos.
  
# Resultados
Podemos rejeitar a hipótese nula, ou seja, podemos rejeitar que o tempo médio da viagem nos sábados independem se a condição do tempo é boa ou ruim. Para testar esta hipótese utilizei o método de Igualdade entre as médias de duas populações, principalmente devido ao fato da diferença de tamanho entre os conjuntos de dados, caso estivessem iguais, teria utilizado o dados da mesma população onde a diferença entre elas seriam a condição de tempo.
Aprendizados

* Consultas SQL: extração de direto de bancos de dados utilizando SQL.
* Análise de dados: interpretação e extração de insights valiosos a partir de dados.
* Manipulação de tabelas: reorganização e transformação de dados para facilitar a análise.
* Criação de gráficos: utilização de bibliotecas como Matplotlib, Seaborn para visualizar dados de maneira intuitiva e informativa.
* Formulação de hipóteses: desenvolvimento e teste de suposições sobre o comportamento dos clientes com base nos dados.
* Documentação de projetos: elaboração de documentação clara e detalhada para garantir que o projeto seja compreensível e replicável.
* Utilização de bibliotecas e ferramentas: aplicação prática de diversas bibliotecas e ferramentas do ecossistema Python.
* Tomada de decisões baseadas em dados: uso de insights derivados da análise de dados para orientar decisões estratégicas.
