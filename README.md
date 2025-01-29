# Projeto de Extração e Análise de Repositórios do GitHub

## Introdução

Bem-vindo ao projeto de extração e análise de repositórios do GitHub! Este projeto foi desenvolvido para extrair dados dos repositórios de grandes empresas, como Amazon, Netflix e Spotify, e analisar as linguagens de programação mais utilizadas por elas. Utilizamos a API do GitHub para realizar a extração dos dados e a biblioteca Pandas para transformá-los e analisá-los.

## Objetivo

O objetivo deste projeto é criar um pipeline de ETL (Extração, Transformação e Carregamento) que automatize a extração de dados dos repositórios do GitHub, transforme esses dados em um formato adequado para análise e os carregue em um repositório do GitHub para que possam ser acessados e analisados por outros times da empresa.

## Estrutura do Projeto

O projeto está organizado em três principais arquivos Python:

1. **dados_repos.py**: Responsável pela extração e transformação dos dados dos repositórios do GitHub.
2. **manipula_repos.py**: Responsável pela criação de repositórios e upload dos arquivos transformados para o GitHub.


## Requisitos

Para executar este projeto, você precisará das seguintes bibliotecas Python:

- requests
- pandas
- base64

Você pode instalar todas as dependências utilizando o arquivo `requirements.txt`:

```bash
pip install -r requirements.txt
```

## Configuração

Antes de executar os scripts, você precisará configurar um token de acesso pessoal do GitHub. Este token deve ser armazenado em uma variável de ambiente chamada `GITHUB_TOKEN`. Para configurar a variável de ambiente, siga os passos abaixo:

1. No Linux/macOS, rode:
    ```bash
    export GITHUB_TOKEN="seu_token_aqui"
    ```
2. No Windows (PowerShell):
    ```powershell
    $env:GITHUB_TOKEN="seu_token_aqui"
    ```

## Execução

### Extração e Transformação dos Dados

Para extrair e transformar os dados dos repositórios do GitHub, execute o script `dados_repos.py`:

```bash
python3 dados_repos.py
```

Este script irá extrair os dados dos repositórios das empresas Amazon, Netflix e Spotify, transformá-los em dataframes e salvá-los em arquivos CSV na pasta `dados`.

### Upload dos Arquivos para o GitHub

Para criar um repositório no GitHub e fazer o upload dos arquivos CSV, execute o script `manipula_repos.py`:

```bash
python3 manipula_repos.py
```

Este script irá criar um repositório no GitHub (caso ainda não exista) e fazer o upload dos arquivos CSV gerados pelo script anterior.


## Conclusão

Este projeto demonstra como é possível automatizar a extração, transformação e carregamento de dados dos repositórios do GitHub utilizando Python e a API do GitHub. Com este pipeline de ETL, é possível obter insights valiosos sobre as linguagens de programação mais utilizadas por grandes empresas e compartilhar esses dados com outros times da empresa.

Esperamos que este projeto seja útil e inspire você a criar seus próprios pipelines de ETL para análise de dados!
