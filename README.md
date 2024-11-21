# Pipeline ETL Simples

Este projeto implementa um pipeline ETL (Extract, Transform, Load) básico para extrair dados de um arquivo CSV e uma API, transformá-los e carregá-los em um banco de dados SQLite.

## Uso

1. **Instalação:** Instale as bibliotecas necessárias: `pip install pandas requests sqlalchemy`.

2. **Configuração:**
    * Substitua `'seu_banco_de_dados.db'` pelo caminho para o seu arquivo de banco de dados SQLite.
    * Substitua `'seu_arquivo.csv'` pelo caminho para o seu arquivo CSV.
    * Substitua `'https://sua_api.com/endpoint'` pela URL da sua API.
    * Ajuste a função `transformar_dados` para realizar as transformações necessárias para seus dados.

3. **Execução:** Execute o notebook `pipeline_etl.ipynb`.

4. **Agendamento (opcional):**  Para automatizar a execução do ETL, use o cron (Linux/macOS). Veja as instruções no final do notebook.


## Funcionalidades

* `extrair_dados_csv(caminho_arquivo)`: Extrai dados de um arquivo CSV.
* `extrair_dados_api(url_api)`: Extrai dados de uma API.
* `transformar_dados(df1, df2=None)`: Transforma os dados.
* `carregar_dados(df, nome_tabela)`: Carrega os dados no banco de dados.
* `executar_etl(csv_path, api_url, tabela_destino)`: Executa todo o pipeline.


## Próximos passos

* Implementar tratamento de erros mais robusto, incluindo retries e notificações.
* Adicionar validação de dados antes do carregamento.
* Generalizar o código para suportar mais fontes de dados e tipos de banco de dados.
* Usar um orquestrador de ETL como Airflow ou Prefect para pipelines mais complexos.

## Autor

Fernando Torres Ferreira da Silva
fernando-torres@live.com
