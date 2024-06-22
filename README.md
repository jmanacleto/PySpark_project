## Documentação do Código:
Inicialização da Sessão Spark:

## Pipeline de Limpeza e Transformação para Aplicações de IA com PySpark SQL:
Crie um pipeline que lê dados brutos de uma fonte (por exemplo, CSV, banco de dados) usando PySpark SQL.
Realize limpeza, transformações e agregações nos dados.
Prepare os dados para serem usados em modelos de Machine Learning ou outras aplicações de IA.

SparkSession.builder: Inicializa a sessão Spark para interação com o ambiente de execução do Spark.
Definição do Esquema dos Dados:

schema: Define o esquema dos dados que serão utilizados, especificando os tipos de cada coluna.
Dados de Exemplo:

data: Exemplo de dados que serão utilizados para criar o DataFrame.
Criação e Exibição do DataFrame:

spark.createDataFrame(data, schema=schema): Cria o DataFrame df a partir dos dados e do esquema definido.
df.show(): Exibe os dados brutos originais do DataFrame.
Limpeza dos Dados:

cleaned_data = df.filter(col("price") > 0): Filtra os dados para remover produtos com preço menor ou igual a zero.
cleaned_data.show(): Exibe os dados limpos após a filtragem.
Preparação dos Dados para Modelagem:

feature_columns: Lista das colunas relevantes que serão utilizadas como features para modelagem.
VectorAssembler: Cria um vetor de features a partir das colunas selecionadas.
final_data.show(truncate=False): Exibe os dados finais preparados para modelagem, mostrando a coluna features.
Encerramento da Sessão Spark:

spark.stop(): Encerra a sessão Spark após finalizar todas as operações.
Esta documentação fornece uma visão clara de cada etapa do pipeline, explicando as operações realizadas e os métodos utilizados em cada parte do código. Certifique-se de ajustar os caminhos e operações conforme necessário para o seu caso específico de aplicação de IA com PySpark SQL.
