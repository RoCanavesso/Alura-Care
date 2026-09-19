# Alura Care

Projeto de estudo desenvolvido durante o curso
[Machine Learning: lidando com dados de muitas dimensões](https://www.alura.com.br/curso-online-reducao-dimensionalidade),
da Alura.

O projeto reproduz o contexto fictício da **Alura Care**, uma empresa da área da
saúde que deseja investigar se é possível reduzir a quantidade de exames usados
na classificação de um diagnóstico de câncer sem comprometer o desempenho do
modelo de Machine Learning.

> Este repositório tem finalidade exclusivamente educacional. Os dados e os
> resultados obtidos não devem ser utilizados para diagnósticos ou decisões
> médicas.

## Objetivos de aprendizagem

Ao longo do projeto serão explorados os seguintes temas:

- identificação dos desafios de dados com muitas dimensões;
- preparação dos dados e tratamento de valores ausentes;
- construção de um modelo de classificação de referência;
- identificação de atributos constantes e correlacionados;
- análise de correlação com Pandas e Seaborn;
- seleção automática de features com `SelectKBest` e `RFE`;
- redução de dimensionalidade com PCA e t-SNE;
- comparação do desempenho dos modelos antes e depois da seleção de features;
- visualização de dados de alta dimensionalidade em duas dimensões.

## Base de dados

O arquivo `data/raw/exames.csv` contém uma base fictícia inspirada no
Breast Cancer Wisconsin (Diagnostic) Data Set. Atualmente, ela possui:

- 569 registros;
- 35 colunas;
- uma coluna de identificação (`id`);
- uma variável alvo (`diagnostico`), com as classes `M` e `B`;
- 33 variáveis de exames (`exame_1` a `exame_33`).

O objetivo do estudo é descobrir quais dessas variáveis carregam informação
relevante para a classificação e quais podem ser removidas ou representadas em
um espaço de menor dimensionalidade.

## Estrutura do projeto

```text
Alura-Care/
|-- data/
|   `-- raw/
|       `-- exames.csv
|-- notebooks/
|   `-- 01.ipynb
|-- .vscode/
|   `-- settings.json
|-- requirements.txt
`-- README.md
```

- `data/raw/`: dados originais, mantidos sem alterações;
- `notebooks/`: notebooks com as análises e os experimentos do curso;
- `.vscode/settings.json`: configuração do interpretador virtual no VS Code;
- `requirements.txt`: dependências Python necessárias para executar o projeto.

## Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/RoCanavesso/Alura-Care.git
cd Alura-Care
```

### 2. Crie e ative um ambiente virtual

Recomenda-se Python 3.11 ou uma versão mais recente.

No Windows, usando PowerShell:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

No Linux ou macOS:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Instale as dependências

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 4. Registre o ambiente como kernel do Jupyter

```bash
python -m ipykernel install --user --name alura-care-venv --display-name "Python (Alura Care venv)"
```

### 5. Abra o notebook

Pelo JupyterLab:

```bash
jupyter lab notebooks/01.ipynb
```

Também é possível abrir a pasta no VS Code e executar
`notebooks/01.ipynb`. Nesse caso, selecione o kernel
**Python (Alura Care venv)** quando solicitado.

## Situação atual

- [x] Estrutura inicial do repositório criada
- [x] Base de dados adicionada
- [x] Ambiente virtual configurado como kernel do projeto
- [x] Dependências do ambiente documentadas
- [ ] Exploração e preparação dos dados
- [ ] Construção do modelo de referência
- [ ] Seleção de features
- [ ] Aplicação de PCA e t-SNE
- [ ] Comparação e documentação dos resultados

## Tecnologias

- Python
- JupyterLab e Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- scikit-learn

## Referências

- [Curso Machine Learning: lidando com dados de muitas dimensões](https://www.alura.com.br/curso-online-reducao-dimensionalidade)
- [Breast Cancer Wisconsin (Diagnostic) Data Set](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)
