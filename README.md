# 📊 Análise de Linguagens de Programação em Repositórios do GitHub

## Descrição do Projeto

Este projeto tem como objetivo realizar uma extração de dados da API do GitHub para levantar e analisar as linguagens de programação mais utilizadas nos repositórios públicos de três grandes empresas de tecnologia: **Amazon (`amzn`)**, **Netflix (`netflix`)** e **Spotify (`spotify`)**.

O resultado final é um conjunto de arquivos CSV que consolidam o nome de cada repositório e a linguagem de programação principal associada a ele.

## Objetivo

Determinar o panorama das linguagens de programação predominantes utilizadas nos projetos *open-source* da Amazon, Netflix e Spotify, utilizando a API REST do GitHub.

## 🛠️ Tecnologias e Bibliotecas Utilizadas

* **Python 3**
* **requests:** Utilizada para realizar as requisições HTTP e se comunicar com a API do GitHub.
* **pandas:** Utilizada para estruturar, manipular e tratar os dados extraídos em formato de `DataFrame`.

## Metodologia e Estrutura do Código

O desenvolvimento do projeto foi dividido em duas fases: exploração e estruturação final.

### 1. Fase de Exploração (`linguagens_repos_aula1.ipynb`)

O arquivo `linguagens_repos_aula1.ipynb` serviu como um **ambiente de testes e validação**.

* **Foco Inicial:** O *notebook* focou inicialmente em entender a biblioteca `requests` e sua aplicação na API do GitHub.
* **Primeira Extração:** Foi realizada a extração dos dados dos repositórios da **Amazon** (`amzn`).
* **Estruturação de Dados:** Os dados brutos da API foram transformados em um `DataFrame` do Pandas contendo o nome do repositório e a linguagem de programação correspondente.

### 2. Fase de Estruturação Final (`dados_repos.py`)

Após a validação da lógica no *notebook*, o código foi refatorado para o arquivo `dados_repos.py` com o uso de **Programação Orientada a Objetos (POO)**.

* **Classe `DadosRepositorios`:** Uma classe foi criada para encapsular a lógica de extração e processamento de dados para qualquer *owner* (proprietário) de repositório no GitHub.
* **Generalização:** A estrutura POO permitiu aplicar o mesmo código para extrair dados da **Amazon, Netflix e Spotify**.
* **Saída:** O script gera três arquivos `.csv` separados (um para cada empresa) na pasta `dados/` (assumindo que a pasta exista), contendo as colunas `repository_name` e `language`.
