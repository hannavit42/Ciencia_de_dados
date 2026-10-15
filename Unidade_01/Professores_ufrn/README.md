# Docentes da UFRN

### Projeto de teste

O objetivo desse pequeno projeto é aplicar as habilidades da disciplina em dados externos.

O banco de dados em questão é o "Dicionário de Dados - Docentes", obtido em https://dados.ufrn.br/dataset/docentes

## Perguntas norteadoras

- Em quais lotações temos mais professores?
- Qual a distribuição de professores homens e mulheres em lotações da área de STEM?
- Temos mais homens ou mulheres com formação de doutorado e mestrado?

## Estrutura

- `data/`: arquivo `docentes.csv` e o dicionário de dados (`docentesdicionario.pdf`). A pasta não é versionada, então é preciso baixar os arquivos no link acima.
- `notebooks/`: análise exploratória dos dados (`01_EDA.ipynb`).
- `reports/figures/`: gráficos gerados na análise.

## O que a análise faz

1. Importa o `docentes.csv` (2865 docentes, 11 colunas) e confere tipos, valores ausentes e duplicados.
2. Converte `admissao` para data e cria a coluna `anos_trabalho`.
3. Conta professores por lotação e por categoria, e separa o magistério superior do ensino básico, técnico e tecnológico.
4. Limpa os textos (espaços sobrando e `classe_funcional` escrita de dois jeitos).
5. Cruza sexo com lotações de STEM, formação (doutorado e mestrado) e classe funcional.

As lotações de STEM são selecionadas por palavras no nome da lotação, já que o dado não tem uma coluna de área.

## Como executar

1. Baixe `docentes.csv` no link acima e coloque em `data/`.
2. Crie e ative um ambiente virtual e instale as dependências:

```
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

3. Abra `notebooks/01_EDA.ipynb` e execute as células em ordem. O caminho da pasta `data/` no notebook está escrito para a máquina de quem fez o projeto, então ajuste se for necessário.
